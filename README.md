--[[

Si vous n'avez pas sauvegardé au format binaire (rbxl), il est recommandé de sauvegarder immédiatement la partie afin de profiter du format binaire et de préserver les valeurs de certaines propriétés si vous avez utilisé le paramètre IgnoreDefaultProperties (elles pourraient changer).
Pour ce faire, accédez à FICHIER -> Enregistrer sous -> Assurez-vous que le nom de fichier se termine par .rbxl -> Enregistrer.

ServerStorage, ServerScriptService et les scripts serveur sont IMPOSSIBLES à sauvegarder en raison de FilteringEnabled.

Si votre joueur ne peut pas apparaître dans la partie, déplacez les scripts dans StarterPlayer. Exécutez ensuite la commande `game:GetService("Players").CharacterAutoLoads = true`.
Utilisez « Jouer ici » pour démarrer la partie au lieu de « Jouer » pour faire apparaître votre personnage à l'emplacement actuel de votre caméra. Si le système de chat ne fonctionne pas, veuillez utiliser l'explorateur et supprimer tout ce qui se trouve dans le(s) service(s) TextChatService/Chat.
Ou exécutez `game:GetService("Chat"):ClearAllChildren() game:GetService("TextChatService"):ClearAllChildren()`

Si les collisions Union et MeshPart ne fonctionnent pas, exécutez le script ci-dessous dans la barre de commandes Studio :

local C = game:GetService("CoreGui")
local D = Enum.CollisionFidelity.Default

for _, v in game:GetDescendants() do
if v:IsA("TriangleMeshPart") and not v:IsDescendantOf(C) then
v.CollisionFidelity = D
end
end
print("Done")

Si vous ne pouvez pas déplacer la caméra, exécutez ce script dans la barre de commandes Studio :

workspace.CurrentCamera.CameraType = Enum.CameraType.Fixed

Ou détruisez la caméra.

Ce fichier a été généré avec les paramètres suivants : {"SaveBytecode":false,"Callback":false,"ShowStatus":true,"IgnoreDefaultPlayerScripts":true,"NilInstancesFixes":{"BaseWrap":null,"Animator":null,"Attachment":null,"PackageLink":null,"AdPortal":null},"IgnoreList":["CoreGui","CorePackages"],"__DEBUG_MODE":false,"DecompileJobless":false,"IgnoreNotArchivable":true,"RemovePlayerCharacters":true,"Object":false," DecompileIgnore":["TextChatService",null,null],"IgnoreSpecialProperties":true,"TreatUnionsAsParts":true,"IsModel":false,"NilInstances":false,"ExtraInstances":[],"noscripts":false,"ReadMe":true,"scriptcache":true,"OptionsAliases":{"IgnoreArchivable":"IgnoreNotArchivable","DecompileTimeout":"délai d'expiration","SaveNonCreatable":"SaveNotCreatable","SavePlayers":"Isola tePlayers","FileName":"Chemin du fichier","IgnoreDefaultProps":"IgnoreDefaultProperties"},"AlternativeWritefile":true,"mode":"optimisé","SaveCacheInterval":56320,"SharedStringOverwrite":false,"IsolatePlayers":false,"IgnoreSharedStrings":true,"timeout":10,"NotCreatableFixes":["","AnimationTrack","Player","PlayerGui","PlayerScripts","PlayerMouse","ScreenshotHud","St udioData","TextSource","TouchTransmitter"],"Anonymous":false,"IgnoreDefaultProperties":true,"IsolateStarterPlayer":false,"IgnorePropertiesOfNotScriptsOnScriptsMode":false,"IsolateLocalPlayerCharacter":false,"SaveNotCreatable":false,"IsolateLocalPlayer":false,"FilePath":false,"AntiIdle":true,"ShutdownWhenDone":false,"SafeMode":false,"IgnoreProperties":[]}

Temps écoulé : 33.30031859999872, ID de l'emplacement : 3101667897, Version de l'emplacement : 1463, Version du client : 0.684.0.6840690, Exécuteur : Solara 3.0
]]
