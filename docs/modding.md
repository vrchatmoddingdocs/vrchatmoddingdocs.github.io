---
title: Modding Docs
layout: template
filename: modding
--- 

# Melonloader
For any help related to <a href="https://github.com/LavaGang/MelonLoader/"> MelonLoader </a> please visit <a href="https://melonwiki.xyz/#/modders/quickstart"> here </a>


## Patching
Patches are one of the most important things in modding. A patch is a way to call code before (Prefix), or after (Postfix) a specific method is called.

Patching before a method can allow you to change the parameters of the method or even choose if it's called at all.

Postfix patches are very useful for calling code only when you need to, such as when the menu is opened, or when you join a world.

The most common patching library for .net and mono is <a href="https://github.com/pardeike/Harmony">Harmony,</a> which all the example code on this page will be made for.

### Finding Patches
<a href="https://github.com/sinai-dev/UnityExplorer">UnityExplorer</a> is a good tool for finding methods to patch. Using the hook menu, you can check when methods are called live in game.

Here is an example of patching the **OnJoinedRoom** Method from the **NetworkManager** class
```cs
private static readonly MethodInfo LocalJoin = typeof(NetworkManager).GetMethod(nameof(NetworkManager.OnJoinedRoom));

public override void OnApplicationStart()
{
    //Create a HarmonyLib instance.
    HarmonyLib.Harmony instance = new HarmonyLib.Harmony("ExampleInstance");
    //Get the method we want to call after OnLocalJoin is called.
    MethodInfo ourMethod = typeof(ChristmasExample).GetMethod(nameof(OnLocalJoin));
    //Postfix Patch LocalJoin with ourMethod
    //Make sure to use the HarmonyMethod Constructor
    instance.Patch(LocalJoin, null, new HarmonyMethod(ourMethod));
}

public static void OnLocalJoin()
{
    Console.WriteLine("You joined a world!");
}
```

### Future Proofing
Nothing here yet!
