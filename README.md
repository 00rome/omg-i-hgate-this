# Flux (flux.input-buffer)

Build locally (Windows, Geode CLI + SDK installed):

    geode build        # produces build/flux.input-buffer.geode

Or push to GitHub: .github/workflows/build.yml builds on windows-latest and uploads the .geode as an artifact.

If it fails to compile, check these against $GEODE_SDK/bindings/bindings/2.2081/*.bro:
  - GJBaseGameLayer::pushButton / releaseButton signatures
  - CCKeyboardDispatcher::dispatchKeyboardMSG (does it take a `double timestamp`?)
  - GJBaseGameLayer::update, m_gameState.m_levelTime
  - Slider::setValue, SliderThumb::getValue, ButtonSprite::create argument list

## Getting the .geode from GitHub

Push this repo to GitHub, open the Actions tab, run "Build Flux" (or push a commit), then download the `flux-geode` artifact.
