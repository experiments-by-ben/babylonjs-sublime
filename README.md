babylonjs-sublime
===============
Babylonjs sublime adds autocomplete functionallity to javascript files within Sublime Text 3 for BABYLON.js

## Author
Ben

## Installation
Babylonjs sublime can be installed through package control.

- <kbd>Command</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd>
- Package Control Install Package
- Select Babylon.js Autocomplete

## Usage
If everything is installed correctly you should be able to start typing 'BABYLON.' and get auto completion. Enjoy!

## Todos
Next steps would be to add some commonly used code blocks as snippets.  Possible example to create a new scene could be the shortcut

``` javascript
tscene + tab
```

which would pull in the basic code to create a new scene.

``` javascript
var camera, scene, renderer,
    geometry, material, mesh;

    init();
    animate();

    function init() {

        scene = new BABYLON.Scene();

        camera = new BABYLON.PerspectiveCamera( 75, window.innerWidth / window.innerHeight, 1, 10000 );
        camera.position.z = 1000;
        scene.add( camera );

        geometry = new BABYLON.CubeGeometry( 200, 200, 200 );
        material = new BABYLON.MeshBasicMaterial( { color: 0xff0000, wireframe: true } );

        mesh = new BABYLON.Mesh( geometry, material );
        scene.add( mesh );

        renderer = new BABYLON.CanvasRenderer();
        renderer.setSize( window.innerWidth, window.innerHeight );

        document.body.appendChild( renderer.domElement );

    }

    function animate() {

        // note: three.js includes requestAnimationFrame shim
        requestAnimationFrame( animate );
        render();

    }

    function render() {

        mesh.rotation.x += 0.01;
        mesh.rotation.y += 0.02;

        renderer.render( scene, camera );

    }
```
