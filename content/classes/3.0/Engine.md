---
ID_PAGE: 25117
PG_TITLE: Engine
PG_VERSION: 2.1
TAGS:
    -   Engine
---
## Description

class [Engine](/classes/3.0/Engine)

The engine class is responsible for interfacing with all lower-level APIs such as WebGL and Audio.

## Constructor

## new [Engine](/classes/3.0/Engine)(canvas, antialias, options, adaptToDeviceRatio)

@constructor

#### Parameters
 | Name | Type | Description
---|---|---|---
 | canvas | HTMLCanvasElement |      The canvas
optional | antialias | boolean |      True if this engine should support antialiasing, false otherwise.
optional | options | EngineOptions |  - further options to be sent to the getContext function     Can contains these parameters : generateDepthBuffer, generateMipMaps, samplingMode
## Members

### static Instances : [Engine](/classes/3.0/Engine)[]



### static LastCreatedEngine : [Engine](/classes/3.0/Engine)



### static LastCreatedScene : [Scene](/classes/3.0/Scene)



### static NEVER : number



### static ALWAYS : number



### static LESS : number



### static EQUAL : number



### static LEQUAL : number



### static GREATER : number



### static GEQUAL : number



### static NOTEQUAL : number



### static KEEP : number



### static REPLACE : number



### static INCR : number



### static DECR : number



### static INVERT : number



### static INCR_WRAP : number



### static DECR_WRAP : number



### static ALPHA_DISABLE : number

Alpha disable

### static ALPHA_ONEONE : number



### static ALPHA_ADD : number

Add Alpha

### static ALPHA_COMBINE : number

Combine Alpha

### static ALPHA_SUBTRACT : number



### static ALPHA_MULTIPLY : number



### static ALPHA_MAXIMIZED : number



### static ALPHA_PREMULTIPLIED : number



### static ALPHA_PREMULTIPLIED_PORTERDUFF : number



### static ALPHA_INTERPOLATE : number



### static ALPHA_SCREENMODE : number



### static DELAYLOADSTATE_NONE : number

The delay when you don't load

### static DELAYLOADSTATE_LOADED : number

The delay for loaded

### static DELAYLOADSTATE_LOADING : number

The delay of loading

### static DELAYLOADSTATE_NOTLOADED : number

The delay

### static TEXTUREFORMAT_ALPHA : number



### static TEXTUREFORMAT_LUMINANCE : number



### static TEXTUREFORMAT_LUMINANCE_ALPHA : number



### static TEXTUREFORMAT_RGB : number



### static TEXTUREFORMAT_RGBA : number



### static TEXTURETYPE_UNSIGNED_INT : number



### static TEXTURETYPE_FLOAT : number



### static TEXTURETYPE_HALF_FLOAT : number



### static SCALEMODE_FLOOR : number



### static SCALEMODE_NEAREST : number



### static SCALEMODE_CEILING : number



### static Version : string



### static CollisionsEpsilon : number

This member is static : use [Engine](/classes/3.0/Engine).CollisionsEpsilon

Default value : 0.001

### static CodeRepository : string



### static ShadersRepository : string

This member is static : use [Engine](/classes/3.0/Engine).ShadersRepository

Default value : &quot;Babylon/Shaders/&quot;

Used as the source directory of shaders on the host machine

### isFullscreen : boolean

Default value: false

True if fullscreen, false otherwise

### isPointerLock : boolean

Default value: false

True if the pointer is locked, false otherwise

### cullBackFaces : boolean

Default value: true

True if back faces should be culled, false otherwise

### renderEvenInBackground : boolean

Default value: true

If true, the engine will compute all frames even if the app is in background

### preventCacheWipeBetweenFrames : boolean



### enableOfflineSupport : undefined



### scenes : [Scene](/classes/3.0/Scene)[]

An array of [Scene](/classes/3.0/Scene)

### onResizeObservable : [Observable](/classes/3.0/Observable)&lt;[Engine](/classes/3.0/Engine)&gt;

[Observable](/classes/3.0/Observable) event triggered each time the rendering canvas is resized

### onCanvasBlurObservable : [Observable](/classes/3.0/Observable)&lt;[Engine](/classes/3.0/Engine)&gt;

[Observable](/classes/3.0/Observable) event triggered each time the canvas lost focus

### vrDisplaysPromise : any



### static audioEngine : [AudioEngine](/classes/3.0/AudioEngine)



### texturesSupported : Array&lt;string&gt;



### textureFormatInUse : string



### emptyTexture : WebGLTexture



### emptyCubeTexture : WebGLTexture



### webGLVersion : number



### isStencilEnable : boolean

Returns true if the stencil buffer has been enabled through the creation option of the context.

### drawCalls : number

The number of draw calls submitted last frame

### drawCallsPerfCounter : [PerfCounter](/classes/3.0/PerfCounter)



### onLoad : undefined



## Methods

### static MarkAllMaterialsAsDirty(flag, predicate) &rarr; void

Will flag all materials in all scenes in all engines as dirty to trigger new shader compilation

#### Parameters
 | Name | Type | Description
---|---|---|---
 | flag | number | 
optional | predicate | (mat: [Material](/classes/3.0/Material)) =&gt; boolean | 
### resetTextureCache() &rarr; void


### getGlInfo() &rarr; { vendor: string,  renderer: string,  version: string }


### getAspectRatio(camera, useScreen) &rarr; number



#### Parameters
 | Name | Type | Description
---|---|---|---
 | camera | [Camera](/classes/3.0/Camera) |      @param camera
optional | useScreen | boolean |    
### getRenderWidth(useScreen) &rarr; number



#### Parameters
 | Name | Type | Description
---|---|---|---
optional | useScreen | boolean |    

### getRenderHeight(useScreen) &rarr; number



#### Parameters
 | Name | Type | Description
---|---|---|---
optional | useScreen | boolean |    

### getRenderingCanvas() &rarr; HTMLCanvasElement

Returns the rendering canvas
### getRenderingCanvasClientRect() &rarr; ClientRect


### setHardwareScalingLevel(level) &rarr; void

Set the hardware scaling level. The engine is then resized with these new parameters (width/level, height/level).

#### Parameters
 | Name | Type | Description
---|---|---|---
 | level | number |      @param level

### getHardwareScalingLevel() &rarr; number

Returns the hardware scaling level
### getLoadedTexturesCache() &rarr; WebGLTexture[]

Returns all loaded textures from the caches
### getCaps() &rarr; [EngineCapabilities](/classes/3.0/EngineCapabilities)

Returns the engine capabilities
### getDepthFunction() &rarr; number


### setDepthFunction(depthFunc) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | depthFunc | number |   

### setDepthFunctionToGreater() &rarr; void

Set the Depth function to greater
### setDepthFunctionToGreaterOrEqual() &rarr; void

Set the Depth function to greater or equal
### setDepthFunctionToLess() &rarr; void

Set the Depth function to less
### setDepthFunctionToLessOrEqual() &rarr; void

Set the Depth function to less or equal
### getStencilBuffer() &rarr; boolean


### setStencilBuffer(enable) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | enable | boolean |      Set true if the alpha testing is enabled, false otherwise.

### getStencilMask() &rarr; number


### setStencilMask(mask) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | mask | number |  

### getStencilFunction() &rarr; number


### getStencilFunctionReference() &rarr; number


### getStencilFunctionMask() &rarr; number


### setStencilFunction(stencilFunc) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | stencilFunc | number |  

### setStencilFunctionReference(reference) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | reference | number |  

### setStencilFunctionMask(mask) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | mask | number |  

### getStencilOperationFail() &rarr; number


### getStencilOperationDepthFail() &rarr; number


### getStencilOperationPass() &rarr; number


### setStencilOperationFail(operation) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | operation | number |  

### setStencilOperationDepthFail(operation) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | operation | number |  

### setStencilOperationPass(operation) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | operation | number |  

### setDitheringState(value) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | value | boolean |      @param value

### stopRenderLoop(renderFunction) &rarr; void

stop executing a render loop function and remove it from the execution array

#### Parameters
 | Name | Type | Description
---|---|---|---
optional | renderFunction | () =&gt; void |      @param renderFunction

### runRenderLoop(renderFunction) &rarr; void

Register and execute a render loop. The engine can have more than one render function.

@example

engine.runRenderLoop(function () {

     scene.render()

})

#### Parameters
 | Name | Type | Description
---|---|---|---
 | renderFunction | () =&gt; void |      @param renderFunction

### switchFullscreen(requestPointerLock) &rarr; void

Toggle full screen mode.

#### Parameters
 | Name | Type | Description
---|---|---|---
 | requestPointerLock | boolean |      If true, the user requests a pointer lock

### clear(color, backBuffer, depth, stencil) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | color | [Color4](/classes/3.0/Color4) |      The clear color used
 | backBuffer | boolean |      True if this method should clear the color buffer
 | depth | boolean |  
### scissorClear(x, y, width, height, clearColor) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | x | number |      @param x
 | y | number |      @param y
 | width | number |      The width of the rectangle
 | height | number |      The height of the rectangle
### setViewport(viewport, requiredWidth, requiredHeight) &rarr; void

Set the WebGL's viewport

#### Parameters
 | Name | Type | Description
---|---|---|---
 | viewport | [Viewport](/classes/3.0/Viewport) |      @param viewport
optional | requiredWidth | number |      The required width of the viewport. By defaults, equals to the rendering canvas width
optional | requiredHeight | number |      The required height of the viewport. By defaults, equals to the rendering canvas height
### setDirectViewport(x, y, width, height) &rarr; [Viewport](/classes/3.0/Viewport)

Directly set the WebGL [Viewport](/classes/3.0/Viewport)

The x, y, width & height are directly passed to the WebGL call

@return the current viewport Object (if any) that is being replaced by this call. You can restore this viewport later on to go back to the original state.

#### Parameters
 | Name | Type | Description
---|---|---|---
 | x | number |      @param x
 | y | number |      @param y
 | width | number |      The width of the rectangle
### beginFrame() &rarr; void

Method used at the beginning of the frame rendering. Currently, measure the number of frames per seconds (FPS).
### endFrame() &rarr; void

Method used at the end of a frame rendering. Flushes the frame buffer of the canvas.
### resize() &rarr; void

resize the view according to the canvas' size.

@example

  window.addEventListener("resize", function () {

     engine.resize();

  });
### setSize(width, height) &rarr; void

force a specific size of the canvas

#### Parameters
 | Name | Type | Description
---|---|---|---
 | width | number |      The width of the rectangle
 | height | number |      The height of the rectangle
### isVRDevicePresent(callback) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | callback | (result: boolean) =&gt; void |   

### getVRDevice(name, callback) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | name | string | 
 | callback | (device: any) =&gt; void |   
### initWebVR() &rarr; void


### enableVR(vrDevice) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | vrDevice | any |  

### disableVR() &rarr; void


### bindFramebuffer(texture, faceIndex, requiredWidth, requiredHeight) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | texture | WebGLTexture |      @param texture
optional | faceIndex | number |    
optional | requiredWidth | number |      The required width of the viewport. By defaults, equals to the rendering canvas width
### unBindFramebuffer(texture, disableGenerateMipMaps, onBeforeUnbind) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | texture | WebGLTexture |      @param texture
optional | disableGenerateMipMaps | boolean |    
optional | onBeforeUnbind | () =&gt; void | 
### generateMipMapsForCubemap(texture) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | texture | WebGLTexture |      @param texture

### flushFramebuffer() &rarr; void

Flushes the frame buffer
### restoreDefaultFramebuffer() &rarr; void

Restore the default frame buffer
### createUniformBuffer(elements, Float32Array) &rarr; WebGLBuffer



#### Parameters
 | Name | Type | Description
---|---|---|---
 | elements | number[] or Float32Array | 
### createDynamicUniformBuffer(elements, Float32Array) &rarr; WebGLBuffer



#### Parameters
 | Name | Type | Description
---|---|---|---
 | elements | number[] or Float32Array | 
### updateUniformBuffer(uniformBuffer, elements, Float32Array, offset, count) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniformBuffer | WebGLBuffer | 
 | elements | number[] or Float32Array | 
optional | offset | number |      
### createVertexBuffer(vertices, Float32Array) &rarr; WebGLBuffer



#### Parameters
 | Name | Type | Description
---|---|---|---
 | vertices | number[] or Float32Array |      The array of vertices
### createDynamicVertexBuffer(vertices, Float32Array) &rarr; WebGLBuffer



#### Parameters
 | Name | Type | Description
---|---|---|---
 | vertices | number[] or Float32Array |      The array of vertices
### updateDynamicVertexBuffer(vertexBuffer, vertices, Float32Array, offset, count) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | vertexBuffer | WebGLBuffer |      The given vertex buffer
 | vertices | number[] or Float32Array |      The array of vertices
optional | offset | number |      
### createIndexBuffer(indices) &rarr; WebGLBuffer

Create a new index buffer

#### Parameters
 | Name | Type | Description
---|---|---|---
 | indices | IndicesArray |      @param indices

### bindArrayBuffer(buffer) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | buffer | WebGLBuffer |      The buffer

### bindUniformBuffer(buffer) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
optional | buffer | WebGLBuffer |      The buffer

### bindUniformBufferBase(buffer, location) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | buffer | WebGLBuffer |      The buffer
 | location | number | 
### bindUniformBlock(shaderProgram, blockName, index) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | shaderProgram | WebGLProgram |      The given shader program
 | blockName | string | 
 | index | number | 
### updateArrayBuffer(data) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | data | Float32Array |   the data object to associate to the key for this [Engine](/classes/3.0/Engine) instance  the data object to associate to the key for this [Engine](/classes/3.0/Engine) instance   

### recordVertexArrayObject(vertexBuffers, indexBuffer, effect) &rarr; WebGLVertexArrayObject



#### Parameters
 | Name | Type | Description
---|---|---|---
 | vertexBuffers | { [key: string]: [VertexBuffer](/classes/3.0/VertexBuffer) } |      The given vextex buffer
 | indexBuffer | WebGLBuffer |      The given index buffer
 | effect | [Effect](/classes/3.0/Effect) |      @param effect
### bindVertexArrayObject(vertexArrayObject, indexBuffer) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | vertexArrayObject | WebGLVertexArrayObject | 
 | indexBuffer | WebGLBuffer |      The given index buffer
### bindBuffersDirectly(vertexBuffer, indexBuffer, vertexDeclaration, vertexStrideSize, effect) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | vertexBuffer | WebGLBuffer |      The given vertex buffer
 | indexBuffer | WebGLBuffer |      The given index buffer
 | vertexDeclaration | number[] |      The given vertex declaration
 | vertexStrideSize | number |      The given vertex
### bindBuffers(vertexBuffers, indexBuffer, effect) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | vertexBuffers | { [key: string]: [VertexBuffer](/classes/3.0/VertexBuffer) } |      The given vextex buffer
 | indexBuffer | WebGLBuffer |      The given index buffer
 | effect | [Effect](/classes/3.0/Effect) |      @param effect
### unbindInstanceAttributes() &rarr; void


### releaseVertexArrayObject(vao) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | vao | WebGLVertexArrayObject | 

### createInstancesBuffer(capacity) &rarr; WebGLBuffer

Create a dynamic instance buffer

#### Parameters
 | Name | Type | Description
---|---|---|---
 | capacity | number |      The size of this dynamic buffer

### deleteInstancesBuffer(buffer) &rarr; void

Delete an existing instance buffer

#### Parameters
 | Name | Type | Description
---|---|---|---
 | buffer | WebGLBuffer |      The buffer

### updateAndBindInstancesBuffer(instancesBuffer, data, offsetLocations, [InstancingAttributeInfo](/classes/3.0/InstancingAttributeInfo)) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | instancesBuffer | WebGLBuffer |      The instances buffer
 | data | Float32Array |   the data object to associate to the key for this [Engine](/classes/3.0/Engine) instance  the data object to associate to the key for this [Engine](/classes/3.0/Engine) instance   
### applyStates() &rarr; void


### draw(useTriangles, indexStart, indexCount, instancesCount) &rarr; void

Draw

#### Parameters
 | Name | Type | Description
---|---|---|---
 | useTriangles | boolean |      @param useTriangles
 | indexStart | number |      @param indexStart
 | indexCount | number |      @param indexCount
### drawPointClouds(verticesStart, verticesCount, instancesCount) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | verticesStart | number |      
 | verticesCount | number |      
optional | instancesCount | number |      
### drawUnIndexed(useTriangles, verticesStart, verticesCount, instancesCount) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | useTriangles | boolean |      @param useTriangles
 | verticesStart | number |      
 | verticesCount | number |      
### createEffect(baseName, attributesNamesOrOptions, [EffectCreationOptions](/classes/3.0/EffectCreationOptions), uniformsNamesOrEngine, [Engine](/classes/3.0/Engine), samplers, defines, fallbacks, onCompiled, onError, indexParameters) &rarr; [Effect](/classes/3.0/Effect)



#### Parameters
 | Name | Type | Description
---|---|---|---
 | baseName | any |      The base name of the effect (The name of file without .fragment.fx or .vertex.fx)
 | attributesNamesOrOptions | string[] or [EffectCreationOptions](/classes/3.0/EffectCreationOptions) | 
 | uniformsNamesOrEngine | string[] or [Engine](/classes/3.0/Engine) | 
optional | samplers | string[] |      An array of samplers (the objects used to read textures)
optional | defines | string |      The shader defines string
optional | fallbacks | [EffectFallbacks](/classes/3.0/EffectFallbacks) |      @param fallbacks
optional | onCompiled | (effect: [Effect](/classes/3.0/Effect)) =&gt; void |      Function launched when the effect is compiled
optional | onError | (effect: [Effect](/classes/3.0/Effect), errors: string) =&gt; void |      Function when error occurs.
### createEffectForParticles(fragmentName, uniformsNames, samplers, defines, fallbacks, onCompiled, onError) &rarr; [Effect](/classes/3.0/Effect)

Compiled/linked your shaders into a simple object.

#### Parameters
 | Name | Type | Description
---|---|---|---
 | fragmentName | string |      The name of the Particules
optional | uniformsNames | string[] |      The uniforms names
optional | samplers | string[] |      An array of samplers (the objects used to read textures)
optional | defines | string |      The shader defines string
optional | fallbacks | [EffectFallbacks](/classes/3.0/EffectFallbacks) |      @param fallbacks
optional | onCompiled | (effect: [Effect](/classes/3.0/Effect)) =&gt; void |      Function launched when the effect is compiled
### createShaderProgram(vertexCode, fragmentCode, defines, context) &rarr; WebGLProgram



#### Parameters
 | Name | Type | Description
---|---|---|---
 | vertexCode | string |      The vertex shader code
 | fragmentCode | string |      The fragment shader code
 | defines | string |      The shader defines string
### getUniforms(shaderProgram, uniformsNames) &rarr; WebGLUniformLocation[]

Return the uniforms location for the given shader program

#### Parameters
 | Name | Type | Description
---|---|---|---
 | shaderProgram | WebGLProgram |      The given shader program
 | uniformsNames | string[] |      The uniforms names
### getAttributes(shaderProgram, attributesNames) &rarr; number[]

Return the attributes for the given shader program

#### Parameters
 | Name | Type | Description
---|---|---|---
 | shaderProgram | WebGLProgram |      The given shader program
 | attributesNames | string[] |      The name of the attributes
### enableEffect(effect) &rarr; void

Enable effect

#### Parameters
 | Name | Type | Description
---|---|---|---
 | effect | [Effect](/classes/3.0/Effect) |      @param effect

### setIntArray(uniform, array) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | array | Int32Array |      
### setIntArray2(uniform, array) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | array | Int32Array |      
### setIntArray3(uniform, array) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | array | Int32Array |      
### setIntArray4(uniform, array) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | array | Int32Array |      
### setFloatArray(uniform, array) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | array | Float32Array |      
### setFloatArray2(uniform, array) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | array | Float32Array |      
### setFloatArray3(uniform, array) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | array | Float32Array |      
### setFloatArray4(uniform, array) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | array | Float32Array |      
### setArray(uniform, array) &rarr; void

Set array of given shader

#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | array | number[] |      
### setArray2(uniform, array) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | array | number[] |      
### setArray3(uniform, array) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | array | number[] |      
### setArray4(uniform, array) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | array | number[] |      
### setMatrices(uniform, matrices) &rarr; void

Set matrices for a given shader

#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | matrices | Float32Array |      @param matrices
### setMatrix(uniform, matrix) &rarr; void

Set matrix for a given shader

#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | matrix | [Matrix](/classes/3.0/Matrix) |      @param matrix
### setMatrix3x3(uniform, matrix) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | matrix | Float32Array |      @param matrix
### setMatrix2x2(uniform, matrix) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | matrix | Float32Array |      @param matrix
### setFloat(uniform, value) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | value | number |      @param value
### setFloat2(uniform, x, y) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | x | number |      @param x
 | y | number |      @param y
### setFloat3(uniform, x, y, z) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | x | number |      @param x
 | y | number |      @param y
### setBool(uniform, bool) &rarr; void

Set bool for this given shader

#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | bool | number |      @param bool
### setFloat4(uniform, x, y, z, w) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | x | number |      @param x
 | y | number |      @param y
 | z | number |      The z axis
### setColor3(uniform, color3) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | color3 | [Color3](/classes/3.0/Color3) |      The color of the shader
### setColor4(uniform, color3, alpha) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | uniform | WebGLUniformLocation |      The uniforms of the shader
 | color3 | [Color3](/classes/3.0/Color3) |      The color of the shader
 | alpha | number |      The alpha of the shader
### setState(culling, zOffset, force, reverseSide) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | culling | boolean |      @param culling
optional | zOffset | number |      
optional | force | boolean |      @param force
### setDepthBuffer(enable) &rarr; void

Enable or disable the depth buffer

#### Parameters
 | Name | Type | Description
---|---|---|---
 | enable | boolean |      Set true if the alpha testing is enabled, false otherwise.

### getDepthWrite() &rarr; boolean

Get the depth mask
### setDepthWrite(enable) &rarr; void

Enables or disables the depth mask

#### Parameters
 | Name | Type | Description
---|---|---|---
 | enable | boolean |      Set true if the alpha testing is enabled, false otherwise.

### setColorWrite(enable) &rarr; void

Enables or disables the writing or red, blue, green and alpha

#### Parameters
 | Name | Type | Description
---|---|---|---
 | enable | boolean |      Set true if the alpha testing is enabled, false otherwise.

### setAlphaConstants(r, g, b, a) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | r | number | 
 | g | number | 
 | b | number | 
### setAlphaMode(mode, noDepthWriteChange) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | mode | number |      @param mode
optional | noDepthWriteChange | boolean |   
### getAlphaMode() &rarr; number


### setAlphaTesting(enable) &rarr; void

Enables or disables the alpha testing

#### Parameters
 | Name | Type | Description
---|---|---|---
 | enable | boolean |      Set true if the alpha testing is enabled, false otherwise.

### getAlphaTesting() &rarr; boolean

Returns true if the alpha testing is enabled, false otherwise.
### wipeCaches(bruteForce) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
optional | bruteForce | boolean | 

### setTextureFormatToUse(formatsAvailable) &rarr; string

Set the compressed texture format to use, based on the formats you have, and the formats

supported by the hardware / browser.

         * Khronos [Texture](/classes/3.0/Texture) Container (.ktx) files are used to support this.  This format has the

advantage of being specifically designed for OpenGL.  Header elements directly correspond

to API arguments needed to compressed textures.  This puts the burden on the container

generator to house the arcane code for determining these for current & future formats.

         * for description see https://www.khronos.org/opengles/sdk/tools/KTX/

for file layout see https://www.khronos.org/opengles/sdk/tools/KTX/file_format_spec/

         * Note: The result of this call is not taken into account when a texture is base64.

         * @param {Array<string>} formatsAvailable- The list of those format families you have created

on your server.  Syntax: '-' + format family + '.ktx'.  (Case and order do not matter.)

         * Current families are astc, dxt, pvrtc, etc2, & etc1.

@returns The extension selected.

#### Parameters
 | Name | Type | Description
---|---|---|---
 | formatsAvailable | Array&lt;string&gt; |  

### createTexture(urlArg, noMipmap, invertY, scene, samplingMode, onLoad, onError, buffer, HTMLImageElement, fallBack, format) &rarr; WebGLTexture

Usually called from BABYLON.[Texture](/classes/3.0/Texture).ts.  Passed information to create a WebGLTexture.

                        1. A conventional http URL, e.g. 'http://...' or 'file://...'

                        2. A base64 string of in-line texture data, e.g. 'data:image/jpg;base64,/...'

                        3. An indicator that data being passed using the buffer parameter, e.g. 'data:mytexture.jpg'

         * @param {boolean} noMipmap- When true, no mipmaps shall be generated.  Ignored for compressed textures.  They must be in the file.

         * @returns {WebGLTexture} for assignment back into BABYLON.[Texture](/classes/3.0/Texture)

#### Parameters
 | Name | Type | Description
---|---|---|---
 | urlArg | string | 
 | noMipmap | boolean |      Set true if you want to activate Mipmap, false otherwise.
 | invertY | boolean |      @param invertY
 | scene | [Scene](/classes/3.0/Scene) |      The scene where the cube texture
optional | samplingMode | number |      
optional | onLoad | () =&gt; void |      Function when load.
optional | onError | () =&gt; void |      Function when error occurs.
optional | buffer | ArrayBuffer or HTMLImageElement |      The buffer
optional | fallBack | WebGLTexture | 
### updateRawTexture(texture, data, format, invertY, compression) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | texture | WebGLTexture |      @param texture
 | data | ArrayBufferView |   the data object to associate to the key for this [Engine](/classes/3.0/Engine) instance  the data object to associate to the key for this [Engine](/classes/3.0/Engine) instance   
 | format | number |      
 | invertY | boolean |      @param invertY
### createRawTexture(data, width, height, format, generateMipMaps, invertY, samplingMode, compression) &rarr; WebGLTexture



#### Parameters
 | Name | Type | Description
---|---|---|---
 | data | ArrayBufferView |   the data object to associate to the key for this [Engine](/classes/3.0/Engine) instance  the data object to associate to the key for this [Engine](/classes/3.0/Engine) instance   
 | width | number |      The width of the rectangle
 | height | number |      The height of the rectangle
 | format | number |      
 | generateMipMaps | boolean |      True if you want to generate Mipmap, false otherwise.
 | invertY | boolean |      @param invertY
 | samplingMode | number |      
### createDynamicTexture(width, height, generateMipMaps, samplingMode) &rarr; WebGLTexture



#### Parameters
 | Name | Type | Description
---|---|---|---
 | width | number |      The width of the rectangle
 | height | number |      The height of the rectangle
 | generateMipMaps | boolean |      True if you want to generate Mipmap, false otherwise.
### updateTextureSamplingMode(samplingMode, texture) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | samplingMode | number |      
 | texture | WebGLTexture |      @param texture
### updateDynamicTexture(texture, canvas, invertY, premulAlpha, format) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | texture | WebGLTexture |      @param texture
 | canvas | HTMLCanvasElement |      The canvas
 | invertY | boolean |      @param invertY
optional | premulAlpha | boolean | 
### updateVideoTexture(texture, video, invertY) &rarr; void

Update the given dynamic texture with the video given in parameter

#### Parameters
 | Name | Type | Description
---|---|---|---
 | texture | WebGLTexture |      @param texture
 | video | HTMLVideoElement |      The video
 | invertY | boolean |      @param invertY
### createRenderTargetTexture(size, options) &rarr; WebGLTexture

Create a new render target texture
old version had a &quot;generateMipMaps&quot; arg instead of options.
if options.generateMipMaps is undefined, consider that options itself if the generateMipmaps value
in the same way, generateDepthBuffer is defaulted to true

#### Parameters
 | Name | Type | Description
---|---|---|---
 | size | any |      Can be an object with the two parameters width and height.
 | options | any |      Can contains these parameters : generateDepthBuffer, generateMipMaps, samplingMode
### createMultipleRenderTarget(size, options) &rarr; WebGLTexture[]



#### Parameters
 | Name | Type | Description
---|---|---|---
 | size | any |      Can be an object with the two parameters width and height.
 | options | any |      Can contains these parameters : generateDepthBuffer, generateMipMaps, samplingMode
### updateRenderTargetTextureSampleCount(texture, samples) &rarr; number



#### Parameters
 | Name | Type | Description
---|---|---|---
 | texture | WebGLTexture |      @param texture
 | samples | number | 
### createRenderTargetCubeTexture(size, options) &rarr; WebGLTexture



#### Parameters
 | Name | Type | Description
---|---|---|---
 | size | number |      Can be an object with the two parameters width and height.
optional | options | any |      Can contains these parameters : generateDepthBuffer, generateMipMaps, samplingMode
### createCubeTexture(rootUrl, scene, files, noMipmap, onLoad, onError, format) &rarr; WebGLTexture



#### Parameters
 | Name | Type | Description
---|---|---|---
 | rootUrl | string |      @param rootUrl
 | scene | [Scene](/classes/3.0/Scene) |      The scene where the cube texture
 | files | string[] |    
optional | noMipmap | boolean |      Set true if you want to activate Mipmap, false otherwise.
optional | onLoad | () =&gt; void |      Function when load.
optional | onError | () =&gt; void |      Function when error occurs.
### updateTextureSize(texture, width, height) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | texture | WebGLTexture |      @param texture
 | width | number |      The width of the rectangle
 | height | number |      The height of the rectangle
### updateRawCubeTexture(texture, data, format, type, invertY, compression, level) &rarr; void



#### Parameters
 | Name | Type | Description
---|---|---|---
 | texture | WebGLTexture |      @param texture
 | data | ArrayBufferView[] |   the data object to associate to the key for this [Engine](/classes/3.0/Engine) instance  the data object to associate to the key for this [Engine](/classes/3.0/Engine) instance   
 | format | number |      
 | type | number |   
 | invertY | boolean |      @param invertY
optional | compression | string | 
### createRawCubeTexture(data, size, format, type, generateMipMaps, invertY, samplingMode, compression) &rarr; WebGLTexture



#### Parameters
 | Name | Type | Description
---|---|---|---
 | data | ArrayBufferView[] |   the data object to associate to the key for this [Engine](/classes/3.0/Engine) instance  the data object to associate to the key for this [Engine](/classes/3.0/Engine) instance   
 | size | number |      Can be an object with the two parameters width and height.
 | format | number |      
 | type | number |   
 | generateMipMaps | boolean |      True if you want to generate Mipmap, false otherwise.
 | invertY | boolean |      @param invertY
 | samplingMode | number |      
### createRawCubeTextureFromUrl(url, scene, size, format, type, noMipmap, callback, mipmmapGenerator) &rarr; (url, scene, size, format, type, noMipmap, callback, mipmmapGenerator)



#### Parameters
 | Name | Type | Description
---|---|---|---
 | url | string |      The texture url
 | scene | [Scene](/classes/3.0/Scene) |      The scene where the cube texture
 | size | number |      Can be an object with the two parameters width and height.
 | format | number |      
 | type | number |   
 | noMipmap | boolean |      Set true if you want to activate Mipmap, false otherwise.
 | callback | (ArrayBuffer: ArrayBuffer) =&gt; ArrayBufferView[] |   
