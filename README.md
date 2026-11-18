# Lighting Client

**Lighting Client** is a browser-based Minecraft 1.8 client built on an open-source browser Minecraft codebase. This repository contains the Gradle workspace and build targets for the JavaScript and experimental WebAssembly GC runtimes.

> Technical note: Internal compatibility identifiers and required upstream attribution notices are retained. The public-facing project name is Lighting Client.

## Build requirements

- Java 17 or greater (recommended and configured by the Gradle toolchain)
- Gradle wrapper included in this repository

## Build the JavaScript client

Run the `MakeOfflineDownload` script in `target_teavm_javascript`, or run the `makeMainOfflineDownload` Gradle task from your IDE. The build generates `classes.js`, `assets.epk`, and offline downloads in the `javascript` output folder.

## Build the WASM-GC client

Run the `MakeWASMClientBundle` script in `target_teavm_wasm_gc`, or run the `makeMainWasmClientBundle` Gradle task. This generates `assets.epw` and an offline download in `javascript_dist`. The WASM-GC runtime uses a [custom TeaVM fork](https://github.com/Eaglercraft-TeaVM-Fork/eagler-teavm).

## Desktop debug runtime

Run `StartDesktopRuntime` in `target_lwjgl_desktop`, or the existing desktop debug Gradle task (`eaglercraftDebugRuntime`). This LWJGL runtime is intended for development and debugging, not end-user distribution. Always test the browser JavaScript/WASM builds as well.

## Upstream project

Lighting Client is based on an open-source Minecraft 1.8 browser client. See [LIGHTING_CLIENT_TECHNICAL_README.md](LIGHTING_CLIENT_TECHNICAL_README.md) for technical background and feature documentation. Preserve applicable upstream notices and licenses when redistributing.
