## Notes for beginners

- **A few short cuts:**
  - G - Toggle game mode
  - ctrl + 1 (a number) - book a bookmark [A setted sence view]
  - 1 (the same number ↑) - retreive bookmark
  - F - focus on selected object
  - Alt + Mouse dragging - duplicate  
  - ctrl + G - Group
- **Migrate assets between several projects** (*Assets panel - Assets action - Migrate*)
- **Abmient light** - skylight
- Disable "SkyShpere" when rotating the directional light (change the position of the sun). After it updated, re-enable "SkySphere" and click refresh material (*Detial panel - default*)
- **Actor**: is a kind of container like levels 

***
- **Show Hidden Properties**: Could use to show detail properties **during play mode**
- **Compare details**: Multiple detail panels and lock a detail panel;
- **Property matrix** could see or change common attributes between objects
- Could **asign colors to folders**
- *View Options -> Thumbnail Edit Mode* - could **edit objects like models in the content browser panel**.
- **Collections**: Local Short cuts of assets (Also could save a search result to a collection)
- Settings below *Settings -> Scalability* **only change setting in the editor view** rather than the final product.
- *Project setting -> Project -> Maps & Modes* - Change the **play modes** of current project.
- **kill z**: The vertical axis value that the editor will destory objects below the kill z value.

***
- Folders including **.vs** & **Binaries** could be deleted when trying to save space. Also, when some weird problems came up, it is an option to delete the **Binaries** folder to reset the project back to scratch.
- DDC - [The Drive Data Cache](https://docs.unrealengine.com/en-US/ProductionPipelines/DerivedDataCache/index.html): Stores the versions of assets for the target Unreal platforms;
  - Is possible to customized DDC in a shared folder so that other people would not need to re-generated it.

***
- Textures size needs to be power of 2 so that Unreal engine will generate MidMaps for LOD.
- Embedded alpha VS Seperate alpha : 
  - Unreal Engine didn't compressed the alpha pass for textures. 
  - Seperate Alpha will allow to control Alpha seperately. (Like control size)
  
- ![](SRGBUnchecked.png) When **sRGB is unchecked**, sampler type needs to be **Masks**. Because Masks controlled the display area and shouldn't be gamma correction.
- ![](TextureFormats.jpg)
-  MidMap filtering - solve shimmering by adjust Detail -> LOD -> MipMap and choose sharpen or blur.
- Texture Group ![](TextureGroup.jpg) 

***
- Slides:[](Building%20Better%20Pipelines%20for%20Unreal%20Engine%204.pptx)
- 1 Unreal Unit = 1 Centimeter (Make DCC software are set [*Customized -> Units Setup -> System Unit Setup -> 1 Unit = 1 Cetermiters*])
- Light map UV of a model needs to on **0-1 UV space**.
  - ![](LightMapUV.png)  
  - 3D Max UV channel setting needs to be **Chanel 2** [Count start from 1]
  - Unreal Light Map Index needs to be **1** [Count start from 0]

- Auto generate collision for organic models: *Static Mesh -> Convex Decomposi -> Apply*
- Limiting Overdraw : Reduce overdraw (transparent dead areas) in textures ![](LimitingOverdraw.jpg)

- Auto Re-Import - Could track a shared file so that be part of source control ![](AutoRe-Import.jpg)

- Texture needs to be converted to paramter in order to be controlled at Material.
- ![](TextureParam.jpg)

- A glass exampple ![](AGlassExample.jpg)
- **Material Function** - Allows to share a particular piece of material code
- Similar to a customized packaged function that could be used in different material instances.