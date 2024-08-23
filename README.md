# Minimal repro: TS Error with React Leaflet

Minimal repro demonstrating a typescript error with [react-leaflet](https://github.com/PaulLeCam/react-leaflet).

## Steps to reproduce

1. `npm install`
2. `npm run check`

This runs a TS check (i.e. `--noEmit`) and produces the following errors:

```
node_modules/react-leaflet/lib/LayersControl.d.ts:9:65 - error TS2307: Cannot find module '@react-leaflet/core/lib/context' or its corresponding type declarations.

9     layerContainer?: import("leaflet").LayerGroup<any> | import("@react-leaflet/core/lib/context").ControlledLayer | undefined;
                                                                  ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

node_modules/react-leaflet/lib/LayersControl.d.ts:18:69 - error TS2307: Cannot find module '@react-leaflet/core/lib/context' or its corresponding type declarations.

18         layerContainer?: import("leaflet").LayerGroup<any> | import("@react-leaflet/core/lib/context").ControlledLayer | undefined;
                                                                       ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

node_modules/react-leaflet/lib/LayersControl.d.ts:30:69 - error TS2307: Cannot find module '@react-leaflet/core/lib/context' or its corresponding type declarations.

30         layerContainer?: import("leaflet").LayerGroup<any> | import("@react-leaflet/core/lib/context").ControlledLayer | undefined;
                                                                       ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

node_modules/react-leaflet/lib/SVGOverlay.d.ts:11:65 - error TS2307: Cannot find module '@react-leaflet/core/lib/context' or its corresponding type declarations.

11     layerContainer?: import("leaflet").LayerGroup<any> | import("@react-leaflet/core/lib/context").ControlledLayer | undefined;
                                                                   ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Found 4 errors in 2 files.

Errors  Files
     3  node_modules/react-leaflet/lib/LayersControl.d.ts:9
     1  node_modules/react-leaflet/lib/SVGOverlay.d.ts:11
```
