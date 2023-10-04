# LoRA (Low Rank Adaptation)

LoRA, or **Low Rank Adaptation**, is an optional model that can be appended to the generation. Each LoRA adds a small neural network to the original model, aiming to influence it towards its specific generative goal. By adding `--lora` followed by the name of the LoRA model to be used, you can add it to the generation. 

By default, no LoRAs are used unless specifically asked for by the user.

Up to 5 LoRAs can be used at any single time, but their individual influence is reduced by every additional LoRA model. This is automatically done by Distillery's backend in order to preserve the quality of the generative output, since too many LoRAs may generate additional noise in the final product.

!!! tip "How LoRAs actually work"
    A LoRA is controlled by two main parameters: its **weight**, which determines how strongly its influence must be on the original model's output, and its **activation keywords**, which are the words that must be used in order to let the LoRA know it must work. Distillery is handling the weight of the LoRA automatically, so the only thing the user must focus on is the generation prompt.

While the best LoRAs will always be the ones trained over the model that is invoked for the generation, most LoRAs can be ported from one model checkpoint to another of the same family (that is: SD1.5-based LoRAs work across most SD1.5 model checkpoints, and the same goes for SDXL). 

LoRAs are unique tools at our disposal in the generative art toolkit. Think of them as "cartridges" to the model checkpoints' "consoles".

## Loras for SD 1.5 models

The following LoRAs are available for our standard models (bloodymary, vodka and screwdriver):


| LoRA name  | Creator  | Description  | Activation words  | Available In                        |
|------------|----------|--------------|-------------------|-------------------------------------|
| ```analog``` | [alenknight](https://civitai.com/user/alenknight) | Analog photography | ```analog style``` | [Link](https://civitai.com/models/52648/analog-diffusion-lora) |
| ```anime``` | [Distillery](distillery.dev) | Anime LoRA (balanced) | ```kiri_fox``` | TBD |
| ```animeminimalist``` | [hortacreator](https://civitai.com/user/hortacreator/models) | Minimalist Anime Style | ```anime minimalist``` | [Link](https://civitai.com/models/24833/minimalist-anime-style) |
| ```architecture``` | [xjdeng](https://civitai.com/user/xjdeng/models) | Photorealistic architectural images | ```amazingarchitecture``` | [Link](https://civitai.com/models/107455?modelVersionId=125987) |
| ```atmosphere``` | [Eisthol](https://civitai.com/user/Eisthol/models) | Adds details and ambiance to a scene | ```None``` | [Link](https://civitai.com/models/75164/atmosphere) |
| ```avatarnavi``` | [SeventKnight](https://civitai.com/user/SeventKnight/models) | Transforms characters into Na’vi Avatar aliens | ```na'vi, avatar, blue skin, aoa``` | [Link](https://civitai.com/models/21787/alloutnavi) |
| ```badvhs``` | [zarxrax](https://civitai.com/user/zarxrax/models) | Old, poor-quality VHS tape | ```vhs footage, vhs``` | [Link](https://civitai.com/models/3679/bad-vhs) |
| ```barbie``` | [RIXYN](https://tensor.art/u/628134534906582880) | Makes anything Barbie | ```ts_barbie``` | [Link](https://civitai.com/models/73934/barbie-or-toy-story-3) |
| ```baroque``` | [konyconi](https://civitai.com/user/konyconi/models) | Baroque aesthetics style | ```baroqueAI``` | [Link](https://civitai.com/models/38414/baroqueai) |
| ```battleworn``` | [Endless8](https://civitai.com/user/Endless8/models) | Creates characters is a battle worn state | ```None``` | [Link](https://civitai.com/models/24015/battleworn-concept) |
| ```biomechanical``` | [konyconi](https://civitai.com/user/konyconi/models) | H. R. Giger-inspired biomechanical images | ```hrgiger``` | [Link](https://civitai.com/models/23698?modelVersionId=30077) |
| ```bladerunner``` | [luisa_pinguin](https://twitter.com/LuisaCoolSouza) | Makes Blade Runner 2049 movie stills | ```moviestill``` | [Link](https://civitai.com/models/5566/luisap-bladerunner2049-still-lora) |
| ```bluetheme``` | [phoenix_ms](https://civitai.com/user/phoenix_ms/models) | Creates melancholic blue scenes involving rain and dusk | ```phblue, scenery, blue theme``` | [Link](https://civitai.com/models/76012/rain-blue-and-sarrow-stylescenery) |
| ```boho``` | [konyconi](https://civitai.com/user/konyconi/models) | Boho style, by konyconi | ```bohoai``` | [Link](https://civitai.com/models/51966/bohoai) |
| ```candyland``` | [RIXYN](https://tensor.art/u/628134534906582880) | Background becomes candy (think Sugar Rush from Wreck-it Ralph) | ```candyland, full background``` | [Link](https://civitai.com/models/96639/candyland) |
| ```caravaggio``` | [Ashley_Jones_fan](https://civitai.com/user/Ashley_Jones_fan/models) | Artist LoRA: Caravaggio oil paintings | ```CARAVAGGIO``` | [Link](https://civitai.com/models/119790/caravaggio-oil-painting-style) |
| ```caricature``` | [vizsumit](https://civitai.com/user/vizsumit/models) | Caricature style | ``` caricature``` | [Link](https://civitai.com/models/56978/cartoon-caricature) |
| ```charactersheet``` | [YeiyeiArt](https://tensor.art/u/612567052280105600) | Creates character design sheets | ```CharacterSheet``` | [Link](https://civitai.com/models/100435/character-design-sheet-helper-3-perspectives-comissions-opens-by-yeiyeiart) |
| ```chibi``` | [lucil](https://civitai.com/user/luciI) | Chibi style | ```chibi``` | [Link](https://civitai.com/models/22820/chibi-artstyle) |
| ```cool``` | [Ostris](https://ostris.com/) | Cool temperature colors (blue) | ```None``` | [Link](https://civitai.com/models/127535/color-temperature-slider-lora) |
| ```crayon``` | [Ostris](https://ostris.com/) | Crayon drawing style | ```None``` | [Link](https://civitai.com/models/120853?modelVersionId=131468) |
| ```cyberpunk``` | [konyconi](https://civitai.com/user/konyconi/models) | Cyberpunk aesthetics, by konyconi | ```CyberPunkAI, neon``` | [Link](https://civitai.com/models/77121/neoncyberpunkai) |
| ```darkandlight``` | [Eisthol](https://civitai.com/user/Eisthol/models) | Intricate drawings with deep dark & light contrast | ```None``` | [Link](https://civitai.com/models/24584/dark-and-light) |
| ```darkchaos``` | [DmitryPlsnk](https://civitai.com/user/DmitryPlsnk/models) | Horror: dark, chaotic images | ```chaosmix``` | [Link](https://civitai.com/models/98602?modelVersionId=105462) |
| ```darkfantasy``` | [dabbinggoose](https://civitai.com/user/dabbinggoose) | Dark fantasy drawings | ```None``` | [Link](https://civitai.com/models/24934/dark-fantasy) |
| ```darktheme``` | [rMada](https://civitai.com/user/rMada/models) | Darker images | ```None``` | [Link](https://civitai.com/models/87575) |
| ```davinci``` | [DarkBeam](https://civitai.com/user/DarkBeam) | Artist LoRA: Leonardo da Vinci oil paintings | ```wjqleonardo``` | [Link](https://civitai.com/models/63331/leonardo-da-vinci-style) |
| ```deep``` | [Ostris](https://ostris.com/) | Depth of field: deep | ```None``` | [Link](https://civitai.com/models/135380?modelVersionId=149218) |
| ```detail``` | [rMada](https://civitai.com/user/rMada/models) | Adds details to images | ```None``` | [Link](https://civitai.com/models/87378/difconsistency-detail-pack) |
| ```dragon``` | [IronCatMan](https://civitai.com/user/IronCatMan/models) | Adds dragons as characters | ```dragon``` | [Link](https://civitai.com/models/30151?modelVersionId=36321) |
| ```eldenring``` | [daemonrat](https://civitai.com/user/daemonrat/models) | Elden Ring style | ```elden ring style``` | [Link](https://civitai.com/models/7482/elden-ring-lora-extraction) |
| ```environmentart``` | [Petybear](https://civitai.com/user/Petybear/models) | Environment art & scenery | ```None``` | [Link](https://civitai.com/models/93826?modelVersionId=120191) |
| ```esoteric``` | [Ciro_Negrogni](https://linktr.ee/ciro_negrogni) | Victorian-style occultist/esoteric images | ```victorian_esoteric``` | [Link](https://civitai.com/models/124678/victorian-esoteric) |
| ```fairytale``` | [konyconi](https://civitai.com/user/konyconi/models) | Fairy tale aesthetics, by konyconi | ```FairyTaleAI``` | [Link](https://civitai.com/models/42260/fairytaleai) |
| ```fat``` | [Ostris](https://ostris.com/) | Character weight: fat | ```None``` | [Link](https://civitai.com/models/112552?modelVersionId=126824) |
| ```foodphoto``` | [leroidoesaiart](https://civitai.com/user/leroidoesaiart) | Food photography | ```foodphoto``` | [Link](https://civitai.com/models/45322/food-photography) |
| ```futuristicscape``` | [fitcorder](https://linktr.ee/fitcorder) | Makes detailed, futuristic spaces and landscapes | ```None``` | [Link](https://civitai.com/models/58764?modelVersionId=92193) |
| ```gameofthrones``` | [Lykon](https://tensor.art/u/600303455797521413) | Game of Thrones style characters and scenery | ```Game of Thrones``` | [Link](https://civitai.com/models/102584/game-of-thrones-style-lora) |
| ```gothicdress``` | [cyberAngel_](https://civitai.com/user/cyberAngel_/models) | Gothic style dress | ```lo_dress``` | [Link](https://civitai.com/models/65283?modelVersionId=116611) |
| ```gothicpunk``` | [konyconi](https://civitai.com/user/konyconi/models) | GothicPunk style | ```GothicPunkAI``` | [Link](https://civitai.com/models/78695/gothicpunkai) |
| ```gta``` | [vizsumit](https://civitai.com/user/vizsumit/models) | GTA style drawings | ```comic character``` | [Link](https://civitai.com/models/66719?modelVersionId=161686) |
| ```isometric``` | [CitronLegacy](https://civitai.com/user/CitronLegacy/models) | Isometric views | ```Isometric_Setting``` | [Link](https://civitai.com/models/118775/stylized-setting-isometric) |
| ```isometricdnd``` | [Tomas_Aguilar](https://civitai.com/user/Tomas_Aguilar) | Isometric interiors for D&D/RPG | ```isometricclas2nive, isometricnive``` | [Link](https://civitai.com/models/80719/table-rpg-dandd-maps-isometric-room) |
| ```kiri``` | [Distillery](distillery.dev) | Anime LoRA (strong) | ```kiri_fox``` | TBD |
| ```kurzgesagt``` | [chilon249](https://civitai.com/user/chilon249/models) | Kurzgesagt drawing style | ```kurzgesagt, vector art``` | [Link](https://civitai.com/models/10098?modelVersionId=12006) |
| ```lego``` | [LordJia](https://huggingface.co/lordjia) | Makes anything Lego | ```LEGO Creator, LEGO MiniFig, LEGO BrickHeadz``` | [Link](https://civitai.com/models/92444?modelVersionId=150123) |
| ```lightning``` | [DitamAi](https://twitter.com/DitamAi_) | Create more consistent lightning | ```Lightning, Lighting``` | [Link](https://civitai.com/models/10222/lightningvfx-create-more-consistent-lightning) |
| ```marble``` | [daemonrat](https://civitai.com/user/daemonrat/models) | Makes marble statues | ```marblee style, marblee, marblesh ``` | [Link](https://civitai.com/models/7702/marblesh-lora-extraction) |
| ```mecha``` | [Cinsdia](https://twitter.com/cinsdia?t=oJuy8Qw1BQ5uCXODAlQo5Q&s=09) | Mecha characters | ```mecha``` | [Link](https://civitai.com/models/76693/mecha) |
| ```minimaldrawing``` | [Cinsdia](https://twitter.com/cinsdia?t=oJuy8Qw1BQ5uCXODAlQo5Q&s=09) | Minimalistic hand-drawn art style | ```None``` | [Link](https://civitai.com/models/104597/niji-handdrawminimalistlineart) |
| ```minimalvector``` | [Cinsdia](https://twitter.com/cinsdia?t=oJuy8Qw1BQ5uCXODAlQo5Q&s=09) | Minimalistic vector art style | ```None``` | [Link](https://civitai.com/models/103904/niji-minimal-vector-style) |
| ```modernlogo``` | [leroidoesaiart](https://civitai.com/user/leroidoesaiart/models) | Modern corporate logos | ```modernlogo``` | [Link](https://civitai.com/models/22399/modern-logo) |
| ```neonlight``` | [Eisthol](https://civitai.com/user/Eisthol/models) | Drawings with neon lights | ```neon lights``` | [Link](https://civitai.com/models/50408/neon-light) |
| ```nightmare``` | [konyconi](https://civitai.com/user/konyconi/models) | Horror lora by konyconi | ```NightmarishAI``` | [Link](https://civitai.com/models/56336/nightmarishai) |
| ```nintendo64``` | [name64](https://civitai.com/user/name64/models) | Low Poly, Nintendo 64 style | ```n64style, psxstyle, dsstyle``` | [Link](https://civitai.com/models/85322/icbin64-i-cant-believe-its-not-64) |
| ```noir``` | [YeiyeiArt](https://tensor.art/u/612567052280105600) | Noir style | ```NoirStyle``` | [Link](https://civitai.com/models/125916/film-noir-style-retro-photo-by-yeiyeiart) |
| ```oilpainting``` | [nnna](https://civitai.com/user/nnna/models) | Oil painting style | ```None``` | [Link](https://civitai.com/models/107165/oil-painting-stick) |
| ```pastelcolor``` | [nnna](https://civitai.com/user/nnna/models) | Light colors and pen style | ```None``` | [Link](https://civitai.com/models/130868/pastel-color) |
| ```pencil``` | [L0datmos](https://civitai.com/user/L0datmos/models) | Pencil drawing style | ```None``` | [Link](https://civitai.com/models/110244/drawing) |
| ```pixar``` | [baiteryamato](https://civitai.com/user/baiteryamato/models) | Pixar style | ```pixarstyle``` | [Link](https://civitai.com/models/17303/pixar-style-lora) |
| ```pixelart``` | [luisa_pinguin](https://twitter.com/LuisaCoolSouza) | Pixel art | ```pixel art``` | [Link](https://civitai.com/models/10706/luisap-pixel-art-lora) |
| ```pixhell``` | [SPYBG](https://civitai.com/user/SPYBG/models) | Alternative pixel art LoRA | ```pixelart``` | [Link](https://civitai.com/models/21270/pixhell-15-lora) |
| ```platearmor``` | [axebro](https://civitai.com/models/59925/medieval-style-armor-suit-lora) | Makes characters wear medieval full armor suits | ```armor, medieval armor``` | [Link](https://civitai.com/models/59925/medieval-style-armor-suit-lora) |
| ```playfulcartoon``` | [RexelB](https://civitai.com/user/RexelB/models) | Colorful lineless art style for western drawings | ```playfulwhimsy style, sprinkledpastels style``` | [Link](https://civitai.com/models/18812/playful-whimsy-lineless-illustrations) |
| ```postapocalypse``` | [konyconi](https://civitai.com/user/konyconi/models) | Postapocalypse style | ```postapocalypse``` | [Link](https://civitai.com/models/20665/postapocalypse-5mb-lora-extraction) |
| ```psychedelicnoir``` | [Ciro_Negrogni](https://linktr.ee/ciro_negrogni) | Intricate noir patterns and surreal imagery | ```psychedelic_noir``` | [Link](https://civitai.com/models/120638?modelVersionId=131218) |
| ```realism``` | [Distillery](distillery.dev) | Photorealistic and prompt-compliant generations | ```None``` | [Link](https://civitai.com/models/90467/vodkaportraits-photorealism) |
| ```retrofuturism``` | [konyconi](https://civitai.com/user/konyconi/models) | 1970 retrofuturistic aesthetics | ```1970RetroFuturism``` | [Link](https://civitai.com/models/64235/1970retrofuturism) |
| ```retroscifi``` | [natinitakira](https://civitai.com/user/natinitakira/models) | Imitates artistic renderings of space artists from the 60-70s | ```None``` | [Link](https://civitai.com/models/58839/retro-sci-fi) |
| ```retrowave``` | [DmitryPlsnk](https://civitai.com/user/DmitryPlsnk/models) | Sci-fi/retrowave style | ```retrowave``` | [Link](https://civitai.com/models/73249/retrowave) |
| ```rootsbranches``` | [konyconi](https://civitai.com/user/konyconi/models) | Makes objects sprout roots and branches | ```RootsBranchesAI``` | [Link](https://civitai.com/models/63660/rootsbranchesai) |
| ```saltbae``` | [FallenIncursio](https://civitai.com/user/FallenIncursio/models) | Makes the Salt Bae meme position | ```SaltBaeMeme``` | [Link](https://civitai.com/models/106212/salt-bae-meme-or-concept-lora) |
| ```scifi``` | [Ciro_Negrogni](https://linktr.ee/ciro_negrogni) | Sci-fi imagery | ```None``` | [Link](https://civitai.com/models/100489/sci-fi-xl-style) |
| ```shallow``` | [Ostris](https://ostris.com/) | Depth of field: shallow | ```None``` | [Link](https://civitai.com/models/135380?modelVersionId=149218) |
| ```silhouette``` | [Eisthol](https://civitai.com/user/Eisthol/models) | Dark sillhouette images | ```silhouette, light particles``` | [Link](https://civitai.com/models/28742/light-and-silhouette) |
| ```skull``` | [muf00d](https://civitai.com/user/muf00d/models) | Adds skulls to the generation | ```skull``` | [Link](https://civitai.com/models/82621/skull) |
| ```space``` | [edobgames](https://civitai.com/user/edobgames/models) | Model that enhances images from space | ```space, planet, galaxy, star``` | [Link](https://civitai.com/models/44667/syfyeye1) |
| ```starfield``` | [zantum](https://civitai.com/user/zantum/models) | Starfield style | ```1starfield style``` | [Link](https://civitai.com/models/86638/1starfield) |
| ```starwars``` | [Lykon](https://tensor.art/u/600303455797521413) | Star Wars style | ```star wars``` | [Link](https://civitai.com/models/105329/star-wars-style-lora) |
| ```steampunk``` | [konyconi](https://civitai.com/user/konyconi/models) | Steampunk aesthetics, by konyconi | ```SteampunkAI, CogPunkAI``` | [Link](https://civitai.com/models/59338/steampunk-redone) |
| ```thin``` | [Ostris](https://ostris.com/) | Character weight: thin | ```None``` | [Link](https://civitai.com/models/112552?modelVersionId=126824) |
| ```tiltshift``` | [awcolo](https://civitai.com/user/awcolo/models) | Creates a tilt-shift effect on generations | ```None``` | [Link](https://civitai.com/models/25806/tilt-shift) |
| ```undersea``` | [fitcorder](https://linktr.ee/fitcorder) | Underwater generations, both deep and shallow | ```depths-fc``` | [Link](https://civitai.com/models/59994/undersea-depths-fc-lora) |
| ```vermeer``` | [Ashley_Jones_fan](https://civitai.com/user/Ashley_Jones_fan/models) | Artist LoRA: Vermeer oil paintings | ```VERMEER``` | [Link](https://civitai.com/models/118054/vermeer-oil-painting-style-for-portraits) |
| ```victoriandress``` | [cyberAngel_](https://civitai.com/user/cyberAngel_/models) | Victorian style classical dress | ```lodress``` | [Link](https://civitai.com/models/65283?modelVersionId=116611) |
| ```voidenergy``` | [konyconi](https://civitai.com/user/konyconi/models) | Magical blue-violet setting (good for RPG/fantasy horror) | ```V0id3nergy``` | [Link](https://civitai.com/models/60553/kvoidenergy) |
| ```warm``` | [Ostris](https://ostris.com/) | Warm temperature colors (orange) | ```None``` | [Link](https://civitai.com/models/127535/color-temperature-slider-lora) |
| ```water``` | [DitamAi](https://twitter.com/DitamAi_) | Create more consistent water | ```water, stream of water, water balls``` | [Link](https://civitai.com/models/10750/watervfx-create-more-consistent-water-wip) |
| ```watercolor``` | [Cinsdia](https://twitter.com/cinsdia?t=oJuy8Qw1BQ5uCXODAlQo5Q&s=09) | Watercolor style | ```None``` | [Link](https://civitai.com/models/104707/niji-watercolor) |
| ```westerncartoon``` | [quack_quack_22](https://twitter.com/quack_quack_22) | General-purpose western cartoon style | ```cartoon fanart style``` | [Link](https://civitai.com/models/17800/cartoon-fanart-style) |
| ```witchcraftpunk``` | [konyconi](https://civitai.com/user/konyconi/models) | WitchcraftPunk style | ```WitchcraftPunkAI``` | [Link](https://civitai.com/models/78280/witchcraftpunkai) |
| ```zombie``` | [konyconi](https://civitai.com/user/konyconi/models) | Makes any character a zombie | ```rotungwoka person``` | [Link](https://civitai.com/models/20630/rottingzombies-lora-extraction) |


## Loras for SDXL models

We currently only have one LoRA for SDXL: ```lora nurlens```, a realism LoRA.
