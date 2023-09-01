<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Theatre.js Tutorial</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/fabric.js/6.0.0-rc.1/fabric.js"></script>
    <!-- <script src="https://cdnjs.cloudflare.com/ajax/libs/fabric.js/4.5.0/fabric.min.js"></script> -->
    <style>
      body {
        margin: 0;
        color: white;
        background: grey;
        font-family: sans-serif;
        overflow: hidden;
      }
    </style>
  </head>

  <body>
    <canvas id="canvas" width="1920" height="1080"></canvas>

    <script type="module">
      import 'https://cdn.jsdelivr.net/npm/@theatre/browser-bundles@0.6.0/dist/core-and-studio.js';
      // We can now access Theatre.core and Theatre.studio from here
      const { core, studio } = Theatre;

      studio.initialize(); // Start the Theatre.js UI

      // Initialize Fabric.js canvas
      var canvas = new fabric.Canvas('canvas');
      window.canvas = canvas;
      // Create a sample SVG path
      var pathData = 'M50 50 L100 150 Q150 200 200 150 L250 50 Z';
      var path1 = new fabric.Path(pathData, {
        left: 650,
        top: 150,
        fill: 'yellow',
        stroke: 'red',
        strokeWidth: 5,
        strokeUniform: false,
        objectCaching: false,
      });
      canvas.add(path1);
      // console.log(path.path[0]);

      const project = core.getProject('fabricjs path Animation');
      const sheet = project.sheet('Sheet 1');

      // const path1 = canvas.getObjects()[0];
      path1.on('mousedblclick', (e) => {
        edit();
      });
      const aa = {};
      path1.path.forEach((element, i) => {
        aa['Point' + i] = { ...element };
      });

      function getObjectSizeWithStroke(object) {
        var stroke = new fabric.Point(
          object.strokeUniform ? 1 / object.scaleX : 1,
          object.strokeUniform ? 1 / object.scaleY : 1
        ).multiply(object.strokeWidth);
        return new fabric.Point(
          object.width + stroke.x,
          object.height + stroke.y
        );
      }

      const obj = sheet.object('path1', aa);

      const syncProps = () => {
        studio.transaction(({ set }) => {
          path1.path.forEach((val, i) => {
            val.forEach((val1, ii) => {
              set(obj.props['Point' + i][ii], val1);
            });
          });
        });
      };

      obj.onValuesChange((val) => {
        var newPath = [...path1.path];
        newPath.forEach((element, i) => {
          const ss = [];
          if (val['Point' + i][0]) ss.push(val['Point' + i][0]);
          if (val['Point' + i][1]) ss.push(val['Point' + i][1]);
          if (val['Point' + i][2]) ss.push(val['Point' + i][2]);
          if (val['Point' + i][3]) ss.push(val['Point' + i][3]);
          if (val['Point' + i][4]) ss.push(val['Point' + i][4]);
          if (val['Point' + i][5]) ss.push(val['Point' + i][5]);
          newPath[i] = ss;
        });

        const { left, top } = path1;
        path1._setPath(newPath);
        path1.set({ left, top });
        canvas.requestRenderAll();
      });

      // define a function that can keep the polygon in the same position when we change its
      // width/height/top/left.
      function anchorWrapper(anchorIndex, fn) {
        return function (eventData, transform, x, y) {
          var fabricObject = transform.target,
            pathObj = fabricObject.path[anchorIndex],
            absolutePoint = fabric.util.transformPoint(
              {
                x: pathObj[1] - fabricObject.pathOffset.x,
                y: pathObj[2] - fabricObject.pathOffset.y,
              },
              fabricObject.calcTransformMatrix()
            ),
            actionPerformed = fn(eventData, transform, x, y),
            /* eslint-disable no-unused-vars */
            newDim = fabricObject._setPath(fabricObject.path),
            /* eslint-disable no-unused-vars */
            polygonBaseSize = fabricObject._getNonTransformedDimensions(),
            newX = (pathObj[1] - fabricObject.pathOffset.x) / polygonBaseSize.x,
            newY = (pathObj[2] - fabricObject.pathOffset.y) / polygonBaseSize.y;
          fabricObject.setPositionByOrigin(
            absolutePoint,
            newX + 0.5,
            newY + 0.5
          );
          // dispatch({ type: 'CHANGE_PATH1', payload: fabricObject.path });
          syncProps();

          return actionPerformed;
        };
      }
      // define a function that will define what the control does
      // this function will be called on every mouse move after a control has been
      // clicked and is being dragged.
      // The function receive as argument the mouse event, the current trasnform object
      // and the current position in canvas coordinate
      // transform.target is a reference to the current object being transformed,
      function actionHandler(eventData, transform, x, y) {
        var polygon = transform.target,
          currentControl = polygon.controls[polygon.__corner],
          mouseLocalPosition = polygon.toLocalPoint(
            new fabric.Point(x, y),
            'center',
            'center'
          ),
          polygonBaseSize = polygon._getNonTransformedDimensions(),
          size = polygon._getTransformedDimensions(0, 0),
          finalPointPosition = {
            x:
              (mouseLocalPosition.x * polygonBaseSize.x) / size.x +
              polygon.pathOffset.x,
            y:
              (mouseLocalPosition.y * polygonBaseSize.y) / size.y +
              polygon.pathOffset.y,
          };
        polygon.path[currentControl.pointIndex][1] = finalPointPosition.x;
        polygon.path[currentControl.pointIndex][2] = finalPointPosition.y;
        // dispatch({ type: 'CHANGE_PATH1', payload: polygon.path });

        return true;
      }
      function actionHandler2(eventData, transform, x, y) {
        var polygon = transform.target,
          currentControl = polygon.controls[polygon.__corner],
          mouseLocalPosition = polygon.toLocalPoint(
            new fabric.Point(x, y),
            'center',
            'center'
          ),
          polygonBaseSize = polygon._getNonTransformedDimensions(),
          size = polygon._getTransformedDimensions(0, 0),
          finalPointPosition = {
            x:
              (mouseLocalPosition.x * polygonBaseSize.x) / size.x +
              polygon.pathOffset.x,
            y:
              (mouseLocalPosition.y * polygonBaseSize.y) / size.y +
              polygon.pathOffset.y,
          };
        polygon.path[currentControl.pointIndex][3] = finalPointPosition.x;
        polygon.path[currentControl.pointIndex][4] = finalPointPosition.y;
        // dispatch({ type: 'CHANGE_PATH1', payload: polygon.path });

        return true;
      }
      function actionHandler3(eventData, transform, x, y) {
        var polygon = transform.target,
          currentControl = polygon.controls[polygon.__corner],
          mouseLocalPosition = polygon.toLocalPoint(
            new fabric.Point(x, y),
            'center',
            'center'
          ),
          polygonBaseSize = polygon._getNonTransformedDimensions(),
          size = polygon._getTransformedDimensions(0, 0),
          finalPointPosition = {
            x:
              (mouseLocalPosition.x * polygonBaseSize.x) / size.x +
              polygon.pathOffset.x,
            y:
              (mouseLocalPosition.y * polygonBaseSize.y) / size.y +
              polygon.pathOffset.y,
          };
        polygon.path[currentControl.pointIndex][5] = finalPointPosition.x;
        polygon.path[currentControl.pointIndex][6] = finalPointPosition.y;
        // dispatch({ type: 'CHANGE_PATH1', payload: polygon.path });

        return true;
      }

      function renderIcon(icon) {
        return function renderIcon(
          ctx,
          left,
          top,
          styleOverride,
          fabricObject
        ) {
          // var size = this.cornerSize;
          ctx.save();
          //   ctx.translate(left, top);
          //   ctx.rotate(fabric.util.degreesToRadians(fabricObject.angle));
          ctx.font = '35px Georgia';

          ctx.textAlign = 'center';
          ctx.fillText(icon, left, top);
          ctx.restore();
        };
      }

      function edit() {
        // clone what are you copying since you
        // may want copy and paste on different moment.
        // and you do not want the changes happened
        // later to reflect on the copy.
        if (window.canvas.getActiveObjects()[0]?.type === 'path') {
          var poly = window.canvas.getActiveObjects()[0];
          window.canvas.setActiveObject(poly);
          poly.edit = !poly.edit;
          if (poly.edit) {
            var lastControl = poly.path.length - 2;
            poly.cornerStyle = 'circle';
            poly.cornerColor = 'black';
            poly.transparentCorners = false;
            poly.controls = poly.path.reduce(function (acc, point, index) {
              if (index < poly.path.length - 1) {
                acc['p1st' + index] = new fabric.Control({
                  positionHandler: polygonPositionHandler,
                  actionHandler: anchorWrapper(
                    index > 0 ? index - 1 : lastControl,
                    actionHandler
                  ),
                  actionName: 'modifyPolygon',
                  pointIndex: index,
                  render: renderIcon(`${index + 1}0`),
                });
                if (point[0] === 'Q' || point[0] === 'C') {
                  acc['p2nd' + index] = new fabric.Control({
                    positionHandler: polygonPositionHandler2,
                    actionHandler: anchorWrapper(
                      index > 0 ? index - 1 : lastControl,
                      actionHandler2
                    ),
                    actionName: 'modifyPolygon2',
                    pointIndex: index,
                    render: renderIcon(`${index + 1}1`),
                  });
                }
                if (point[0] === 'C') {
                  acc['p3rd' + index] = new fabric.Control({
                    positionHandler: polygonPositionHandler3,
                    actionHandler: anchorWrapper(
                      index > 0 ? index - 1 : lastControl,
                      actionHandler3
                    ),
                    actionName: 'modifyPolygon3',
                    pointIndex: index,
                    render: renderIcon(`${index + 1}2`),
                  });
                }
              }
              return acc;
            }, {});
          } else {
            poly.cornerColor = 'blue';
            poly.cornerStyle = 'rect';
            poly.controls = fabric.Object.prototype.controls;
          }
          poly.hasBorders = !poly.edit;
          window.canvas.requestRenderAll();
        }
      }

      // define a function that can locate the controls.
      // this function will be used both for drawing and for interaction.
      function polygonPositionHandler(dim, finalMatrix, fabricObject) {
        var pathObj = fabricObject.path[this.pointIndex];
        var x = pathObj[1] - fabricObject.pathOffset.x,
          y = pathObj[2] - fabricObject.pathOffset.y;
        return fabric.util.transformPoint(
          { x: x, y: y },
          fabric.util.multiplyTransformMatrices(
            fabricObject.canvas.viewportTransform,
            fabricObject.calcTransformMatrix()
          )
        );
      }
      function polygonPositionHandler2(dim, finalMatrix, fabricObject) {
        var pathObj = fabricObject.path[this.pointIndex];
        var x = pathObj[3] - fabricObject.pathOffset.x,
          y = pathObj[4] - fabricObject.pathOffset.y;
        return fabric.util.transformPoint(
          { x: x, y: y },
          fabric.util.multiplyTransformMatrices(
            fabricObject.canvas.viewportTransform,
            fabricObject.calcTransformMatrix()
          )
        );
      }
      function polygonPositionHandler3(dim, finalMatrix, fabricObject) {
        var pathObj = fabricObject.path[this.pointIndex];
        var x = pathObj[5] - fabricObject.pathOffset.x,
          y = pathObj[6] - fabricObject.pathOffset.y;
        return fabric.util.transformPoint(
          { x: x, y: y },
          fabric.util.multiplyTransformMatrices(
            fabricObject.canvas.viewportTransform,
            fabricObject.calcTransformMatrix()
          )
        );
      }
    </script>
  </body>
</html>
