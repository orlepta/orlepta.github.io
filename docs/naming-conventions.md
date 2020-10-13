
# Naming Conventions

## Naming conventions for entity

### Testo 1

### Testo 3

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas ullamcorper augue id ligula pellentesque commodo. Ut molestie euismod viverra. Morbi elementum sem leo, nec ultricies ante interdum et. Sed non elementum tellus, id mattis magna. Vestibulum interdum, dolor eget auctor molestie, tortor augue dapibus orci, quis lobortis tortor sapien et enim. In vehicula tempus hendrerit. Mauris vitae malesuada augue. Interdum et malesuada fames ac ante ipsum primis in faucibus. Mauris eget fermentum ligula, ac porttitor arcu. Proin semper mi ac velit lacinia tempor non eget velit. Aenean rutrum, sem eget consectetur blandit, neque nulla gravida velit, ac malesuada sapien nunc et lacus.

> An awesome project.

Aliquam viverra purus mauris, in cursus arcu lacinia condimentum. Curabitur sagittis nisl elit, id venenatis tortor maximus at. Nulla fringilla non mauris et laoreet. Fusce ligula sem, tristique sit amet maximus sed, maximus a purus. Donec massa mi, feugiat at tortor eget, semper commodo orci. Nulla mollis sem id eros bibendum dapibus. Ut consequat sagittis nunc, eget blandit leo fermentum id. Suspendisse sem justo, placerat vitae magna sit amet, tincidunt tincidunt sem. Donec tristique nisl ut nulla pulvinar, sit amet tempus arcu viverra. Pellentesque vitae placerat nisl. Morbi ut arcu erat. Praesent rutrum vehicula risus sed commodo. Vivamus sollicitudin mollis rutrum.

### Testo 2

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas ullamcorper augue id ligula pellentesque commodo. Ut molestie euismod viverra. Morbi [elementum sem leo,](http://google.fr) nec ultricies ante interdum et. Sed non elementum tellus, id mattis magna. Vestibulum interdum, dolor eget auctor molestie, tortor augue dapibus orci, quis lobortis tortor sapien et enim. In vehicula tempus hendrerit. Mauris vitae malesuada augue. Interdum et malesuada fames ac ante **ipsum** primis in faucibus. Mauris eget fermentum ligula, ac porttitor arcu. Proin semper mi ac velit lacinia tempor non eget velit. Aenean rutrum, sem eget consectetur blandit, neque nulla gravida velit, ac malesuada sapien nunc et lacus.

Aliquam viverra purus mauris, in cursus arcu lacinia condimentum. Curabitur sagittis nisl elit, id venenatis tortor maximus at. Nulla fringilla non mauris et laoreet. Fusce ligula sem, tristique sit amet maximus sed, maximus a purus. Donec massa mi, feugiat at tortor eget, semper commodo orci. Nulla mollis sem id eros bibendum dapibus. Ut consequat sagittis nunc, eget blandit leo fermentum id. Suspendisse sem justo, placerat vitae magna sit amet, tincidunt tincidunt sem. Donec tristique nisl ut nulla pulvinar, sit amet tempus arcu viverra. Pellentesque vitae placerat nisl. Morbi ut arcu erat. Praesent rutrum vehicula risus sed commodo. Vivamus sollicitudin mollis rutrum.

```js
  private function validateVehicleQQ(vehicle : entity.PersonalVehicle) {
    if (vehicle.VehicleType == null) {
      Result.addFieldError(vehicle, "VehicleType", TC_DEFAULT, 
          DisplayKey.get("Web.Policy.PA.Validation.VehicleTypeRequired"), QQINFO_WIZARD_STEP)
    }
    if (vehicle.CostNew == null) {
      Result.addFieldError(vehicle, "CostNew", TC_DEFAULT, 
          DisplayKey.get("Web.Policy.PA.Validation.CostNewRequired"), QQINFO_WIZARD_STEP)
    } else  if (not vehicle.CostNew.IsPositive) {
      Result.addFieldError(vehicle, "CostNew", TC_DEFAULT, 
          DisplayKey.get("Web.Policy.PA.Validation.PositiveCostNewRequired"), QQINFO_WIZARD_STEP)
    }
  }

  private function atLeastOneVehicle() {
    if (paLine.Vehicles.IsEmpty and Context.isAtLeast(ValidationLevel.TC_DEFAULT)) {
      var msg = DisplayKey.get("Web.Policy.PA.Validation.AtLeastOneVehicle")
      if (Context.isAtLeast(ValidationLevel.TC_QUICKQUOTABLE)) {
        Result.addError(paLine, ValidationLevel.TC_QUICKQUOTABLE, msg, VEHICLES_WIZARD_STEP)
      } else {
        Result.addWarning(paLine, ValidationLevel.TC_DEFAULT, msg, VEHICLES_WIZARD_STEP)
      }
    }
  }
``` 

Aliquam ultricies enim dolor. Nam eleifend ipsum massa. Mauris pharetra interdum mauris, ut dapibus nisl elementum vitae. Cras consequat posuere nunc et consectetur. Aenean ultricies, justo sit amet semper rutrum, mauris velit accumsan lectus, eu rhoncus elit nisi nec ex. Vestibulum dignissim mauris eget volutpat viverra. Nam ipsum velit, tempus ac sapien eu, volutpat finibus tortor. Morbi dapibus enim at est aliquet, eu semper nibh interdum. In finibus nisl at pellentesque elementum. Etiam ac augue in leo ornare imperdiet in nec felis. Integer nunc massa, dignissim vitae magna non, mollis porta enim. Integer tincidunt mollis enim, vel tempor nisl volutpat quis. Pellentesque quam magna, placerat vel rutrum eget, ornare vel nulla. Morbi iaculis quis ipsum in fringilla. Nam erat sem, blandit ac egestas lobortis, sagittis eget augue. Proin scelerisque, ex non laoreet luctus, libero tellus ultrices massa, quis placerat elit turpis sit amet lorem.



## Naming conventions for typelists

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas ullamcorper augue id ligula pellentesque commodo. Ut molestie euismod viverra. Morbi elementum sem leo, nec ultricies ante interdum et. Sed non elementum tellus, id mattis magna. Vestibulum interdum, dolor eget auctor molestie, tortor augue dapibus orci, quis lobortis tortor sapien et enim. In vehicula tempus hendrerit. Mauris vitae malesuada augue. Interdum et malesuada fames ac ante ipsum primis in faucibus. Mauris eget fermentum ligula, ac porttitor arcu. Proin semper mi ac velit lacinia tempor non eget velit. Aenean rutrum, sem eget consectetur blandit, neque nulla gravida velit, ac malesuada sapien nunc et lacus.

Aliquam viverra purus mauris, in cursus arcu lacinia condimentum. Curabitur sagittis nisl elit, id venenatis tortor maximus at. Nulla fringilla non mauris et laoreet. Fusce ligula sem, tristique sit amet maximus sed, maximus a purus. Donec massa mi, feugiat at tortor eget, semper commodo orci. Nulla mollis sem id eros bibendum dapibus. Ut consequat sagittis nunc, eget blandit leo fermentum id. Suspendisse sem justo, placerat vitae magna sit amet, tincidunt tincidunt sem. Donec tristique nisl ut nulla pulvinar, sit amet tempus arcu viverra. Pellentesque vitae placerat nisl. Morbi ut arcu erat. Praesent rutrum vehicula risus sed commodo. Vivamus sollicitudin mollis rutrum.

Aliquam ultricies enim dolor. Nam eleifend ipsum massa. Mauris pharetra interdum mauris, ut dapibus nisl elementum vitae. Cras consequat posuere nunc et consectetur. Aenean ultricies, justo sit amet semper rutrum, mauris velit accumsan lectus, eu rhoncus elit nisi nec ex. Vestibulum dignissim mauris eget volutpat viverra. Nam ipsum velit, tempus ac sapien eu, volutpat finibus tortor. Morbi dapibus enim at est aliquet, eu semper nibh interdum. In finibus nisl at pellentesque elementum. Etiam ac augue in leo ornare imperdiet in nec felis. Integer nunc massa, dignissim vitae magna non, mollis porta enim. Integer tincidunt mollis enim, vel tempor nisl volutpat quis. Pellentesque quam magna, placerat vel rutrum eget, ornare vel nulla. Morbi iaculis quis ipsum in fringilla. Nam erat sem, blandit ac egestas lobortis, sagittis eget augue. Proin scelerisque, ex non laoreet luctus, libero tellus ultrices massa, quis placerat elit turpis sit amet lorem.
