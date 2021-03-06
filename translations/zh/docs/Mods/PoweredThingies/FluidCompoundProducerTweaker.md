# Powered Thingies :: Fluid Compound Producer

### 导入

```zenscript
import mods.poweredthingies.Tweaker.fluidCompoundTweaker as fct;
```

### Listing Keys, Removing Recipes by Key, Clearing

```zenscript
fct().logKeys()
fct().removeRecipe('liquid:fluid_tf-molten_tesla') // check <logKeys> output for valid keys
fct().clear()
```

### Adding Recipe

##### Signature

```zenscript
addRecipe(output: ILiquidStack, inputA: ILiquidStack, inputB: ILiquidStack)
```

##### Example

```zenscript
fct().addRecipe(<liquid:tf-sewage> * 150, <liquid:water> * 300, <liquid:lava> * 100);
```

### Notes

All of these actions will get cached and ran after the default registry for this machine has finished registering all recipes (including the ones from the custom jsons).