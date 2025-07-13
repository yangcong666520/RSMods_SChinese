# 那些没人要求的 Rocksmith 模组

[![构建状态](https://ci.appveyor.com/api/projects/status/github/Lovrom8/rsmods?svg=true)](https://ci.appveyor.com/project/Lovrom8/rsmods)

## 重要提示：
如果您尝试运行的是2024年12月19日发布的 Steam Learn & Play 版本，那么您无法直接使用 1.2.7.4 版本的模组，需要进行额外操作。
请参考此 GitHub issue 中的说明来使模组正常工作：https://github.com/Lovrom8/RSMods/issues/196#issuecomment-2564077160。
如果您使用的是 Learn & Play 版本，可以随时尝试 1.2.8.0 版本。
## 功能：

* **扩展音域模式 (Extended Range Mode)**
 * Rocksmith 默认不官方支持7弦（或更多弦）的吉他或5弦贝斯，尽管官方也发布了一些低音调的歌曲作为DLC。
因此，借助 DX9、GDI+ 和一些巧妙的逆向工程，当模组检测到歌曲的调音低于设定的阈值时，颜色方案会相应地改变。
这意味着您的大脑再也不会因为最低的弦是红色（通常代表低E弦）而感到困惑，而实际上您需要弹奏的是低B弦！
实际上，所有琴弦的颜色显示都会向下顺移一位。
* **选项**
  1. ZZ 的颜色方案 - 此模式将复制高 B 弦的默认颜色（色盲模式中使用的蓝绿色），并使其与低 B 弦（第7弦）的颜色相匹配 - [查看扩展音域模式的实际效果](https://www.youtube.com/watch?v=FPjFwt-Dpdo)。
请注意，此视频来自一个较旧的模组版本，但其在游戏中的显示方式是相同的，只是现在启用方式是根据调音自动完成的，而不是通过启用“色盲”模式。
2. 自定义颜色方案 - 由您在设置中定义的色盲颜色方案，它将仅在扩展音域模式的歌曲中使用，而常规歌曲将使用正常颜色。
  ** 已知 bug：一些重音空弦或击弦/勾弦 (HO/PO) 标记的颜色会在默认颜色和修改后的扩展音域模式颜色之间闪烁。
调音器中显示的弦钮颜色没有被正确更改。
颜色在歌曲开始时改变，而不是在调音器中，这意味着首次使用扩展音域模式时，调音器中将显示默认颜色。
这也意味着，如果您上次弹奏了一首扩展音域模式的歌曲，然后返回到标准调音的歌曲——调音器中的弦钮仍将显示为扩展音域模式的颜色。
* **自定义歌曲列表标题 (Custom Song List Titles)**
 * 通常这些标题在游戏中是不可自定义的，仅被列为“歌曲列表 1”到“歌曲列表 6”。 现在您可以自定义它们，例如，创建一个只包含 B 标准调音歌曲的列表，或者只包含练习曲的列表等。
 
* **增加/减少歌曲音量 (Add/Decrease Song Volume)**
 * 如果您正在弹奏的歌曲音量异常小，或者震耳欲聋，通过调用游戏使用的 AudioKinetic 音频引擎的功能，您现在可以动态修改音乐音量，而无需进入混音器。

* **切换背景 (Toggle Loft)**
 * 如果您是主播，这个功能可能会特别方便。
音符轨道后的背景（无论是场馆中的人群还是普通的墙壁）现在可以被动态移除，并替换为深色背景。
建议您同时在游戏设置中关闭“场馆模式”(Venue Mode)，这有助于提升一点性能，并确保不显示彩色的舞台灯光。
全黑的背景随后可以在 OBS 中使用亮度抠像 (Luma key) 设置为黑色来“抠掉”（亮度抠像比色度抠像效果更好），从而使您能够让音符高速公路“悬浮”在您使用的任何背景之上。
对您自己游玩或本地录制游戏视频时来说，它只会显示为全黑的背景。
* **选项** - 背景可以在游戏启动时、仅在歌曲中时，或通过按您定义的热键自动关闭。
* **绿幕墙 (Greenscreen Wall)**
 * 类似于切换背景，但仅应用于背景墙。
这会保留音箱和一些其他被“切换背景”功能移除的UI元素。
* **强制重新枚举 (Force ReEnumeration)**
 * 通常在向您的收藏中添加新歌曲后，您必须重启游戏，或进入游戏内商店，游戏才能识别新歌曲。
* **选项**
 1. 自动 - 每隔 X 秒检查是否有新歌曲添加（即使在弹奏歌曲时！）。
 2. 通过进入枚举菜单 - 菜单中的“商店 (SHOP)”现已被替换为“**枚举 (Enumerate)**”，并方便地移到了第二位 **(仅限GUI)**。
 3. 通过热键 - 按下热键强制游戏枚举您的歌曲。
* **移除某些视觉游戏元素**
 * 这同样是如果您是主播（或者只是喜欢屏幕尽可能整洁）可能会觉得方便的功能，您现在可以从屏幕上移除某些元素。
 * **选项**
 1. 琴头 (Headstock)
 2. 天际线 (Skyline) (顶部的动态难度条)
 3. 品丝 (Frets)
 4. 品记 (Inlays)
 5. 品格标记线 (Lane Markers)
 6. 歌词 (Lyrics)
 
* **彩虹琴弦 (Rainbow Strings)**
 * 一个有趣的模组，它会持续改变您琴弦的色相，让它们看起来像彩虹一样！

* **自定义琴弦颜色 (Custom String Colors)**
 * 不一定全是娱乐和游戏，所以除了彩虹之外，您的琴弦也可以永久更改为您自己的颜色设置。
* **移除歌曲预览 (Remove song previews)**
 * 如果您不喜欢在滚动歌曲列表时听到歌曲预览，也可以禁用它们。
* **后台播放音频 (Play audio in background)**
 * 允许您在游戏处于后台时（通过 alt-tab 切出游戏）收听 Rocksmith。
* **线性 Riff Repeater (Linear Riff Repeater)**
 * 默认情况下，Riff Repeater 的速度不是线性的 - 在标准 Rocksmith 2014 中：Riff Repeater 中的 68% 速度 = 50% 的真实速度。
使用此模组后：Riff Repeater 中的 68% 速度 = 68% 的真实速度。
* **启用循环 (Enable looping)**
 * 允许您循环播放歌曲的某些部分。
这与 Riff Repeater 不同，因为它允许您使用专门的快捷键来设置循环的开始和结束时间点来选择片段。
* **允许倒带 (Allow rewinding)**
 * 如果您在一个片段搞砸了并想重试，您可以倒回设定的秒数。
* **自定义不间断播放计时器 (Custom Non-Stop Play timer)**
 * 在不间断播放模式下，歌曲之间的默认计时器是 10.9 秒，很多人觉得这个时间太长了。
使用此模组，您可以更改每首歌之间的间隔时间（由于技术限制，最低可至2秒）。
* **在第二屏幕启动 RS (Start RS on secondary monitor)**
 * 使 Rocksmith 在您的第二台显示器上运行。
不过，请务必注意工具提示！

* **绕过 2+ RealToneCable 弹窗**
 * 允许您在玩单人模式时插入两根 Real Tone Cable。
如果没有这个模组，Rocksmith 会阻止您这样做。
* **备用音频输出采样率 (Alternative sample rates for sound output)**
 * Rocksmith 通常需要 48kHz 的采样率，但这个模组告诉游戏去寻找您设定的采样率。
这样做可以让您使用不支持 48kHz 的耳机/音箱（例如一些蓝牙耳机）。
这无法解决延迟问题，但至少蓝牙耳机可以在游戏里工作了。
* **防止错误的音色 (Prevent buggy tones)**
 * 在弹奏某些歌曲时，音色系统可能会失灵并持续播放清音音色，无论当前启用了哪种音色。
要解决这个问题，您通常需要重启游戏才能让音色恢复正常，但这个模组可能帮助游戏在不重启的情况下恢复。
* **吉他语音控制 (GuitarSpeak)**
 * 在这个神秘名字背后隐藏着一个激动人心的功能，它能让您通过弹奏吉他上的特定音符来控制游戏（完全可自定义！）。
忘掉您的键盘和鼠标吧，吉他才是王道！
有一个选项可以在调音器中继续使用它 - 默认是关闭的，因为它可能导致问题，但如果您乐意在那种情况下继续使用它 - 就点那个按钮吧。
在歌曲中、调音菜单和校准菜单中，它默认是关闭的。
* **自动进入上次使用的个人资料 (Auto enter last used profile)**
 * 也被称为“叉子插吐司机”模组，因其简单而有效，最好与“快速加载”模组结合使用。
这个 DLL 文件会连续发送回车键，以自动进入游戏。
如果 UPLAY 服务器不可用，可能会导致潜在问题，但总的来说，它让您的生活轻松了不少。
* **自动调整您的 Whammy DT (Auto tune your Whammy DT)**
 * 如果您拥有一台 Digitech Whammy DT 并且有能够发送 MIDI 程序控制信号的设备，例如简单的 USB-MIDI 线或音频接口上的 MIDI 输出端口，您可能会发现这个功能很有用 - 无需触摸踏板即可自动将吉他的调音更改为当前歌曲的调音（即使是像 A443 这样的奇特调音也适用）。
将您的 MIDI 线连接到 Whammy DT 的 MIDI IN 端口，在 GUI 设置中选择 MIDI 设备名称，然后在歌曲开始前的调音屏幕上，按 DELETE 键跳过调音并自动激活 Whammy DT 的降调功能。
这假定您的吉他处于 E 标准或 Drop D 调音，以便设置踏板需要升调或降调的步数。
当模组激活时，您会看到 Whammy DT 上的灯亮起，在歌曲结束后的结果屏幕上它会自动停用。
* **允许 Riff Repeater 速度超过 100% (Allow Riff Repeater Speed Above 100)**
 * 如果您觉得《Through the Fire and Flames》还不够快，您现在可以在 Riff Repeater 中以超过 100% 的速度播放它。
:)
 * **选项**
Riff Repeater 速度增量 - 我们建议您在此处使用 2 作为最小值。
这意味着每次按键都会将曲目速度提高 2%。
这让您在歌曲速度方面拥有最大的灵活性。
* **分数截图 (Screenshot Scores)**
 * 如果您热衷于记录自己的进步，您可能想使用这个选项，它会告诉 Steam 为您最新的一次游戏截图。
它使用 Steam 中默认的 F12 快捷键，在显示歌曲结束后的结果屏幕时进行截图。
* **显示当前音符 (Show Current Note)**
 * 虽然我们仍然无法在您弹奏时强制游戏显示暂停菜单的调音器，但您可以启用这个“廉价版”功能来查看您当前弹奏的音符，这样您最终可以达到 100% 的准确率，而不会因为“糟糕的音符检测”而错过那些烦人的推弦。
* **显示歌曲计时器 (Show Song Timer)**
 * 显示您在歌曲中的当前位置的时间戳。
 * **覆盖输入音量 (Override input volume)**
 * 现在您可以把您的吉他或贝斯音量调到 11 了！
Rocksmith 会设定它希望从您的线缆接收的音量，但这个模组允许您绕过该限制，将其更改为您设置的任何值。
* **修复 Oculus 崩溃 (Fix Oculus Crash)**
 * 当您尝试在 PC 连接了 Oculus / Meta 头显的情况下打开 Rocksmith 时，通常会崩溃。
这个模组通过阻止有问题的代码运行来尝试避免崩溃。
它也可能修复 Rocksmith 打开时其他与音频相关的崩溃。
* **快速加载 (Fast Load)** - **仅限GUI**
 * 如果您在 SSD，特别是 NVMe SSD 硬盘上运行游戏，您会喜欢这个功能——它会跳过开场画面，让您在几秒钟内加载游戏。
它可能相当不稳定，但总的来说，只要您不尝试在老旧的机械硬盘上使用它，它就应该能工作。
这不是一个DLL模组！ 这意味着移除DLL文件不会撤销此模组的更改，您需要恢复您的 cache.psarc 文件备份或验证您的Steam文件。
* **自定义调音 (Custom Tunings)** - **仅限GUI**
 * 默认情况下，游戏能识别的调音种类相当有限，在列表中找不到的情况下，它只会显示“自定义调音 (CUSTOM TUNING)”。
那样没什么帮助，对吧？ 但别担心，您现在可以让游戏知道一首 B 标准调音的歌曲确实是 B 标准，而不仅仅是“自定义调音” :(。
 除了我们包含的列表，如果您发现某些调音未被包含在内，您也可以添加自己的调音。 这不是一个DLL模组！ 这意味着移除DLL文件不会撤销此模组的更改，您需要恢复您的 cache.psarc 文件备份或验证您的Steam文件。
 * **菜单中的“退出游戏” (EXIT GAME in the menu)** -
**仅限GUI**
 * 尽管鼠标是个有用的设备，但当您想退出游戏时，它并不是最方便的选择。 到目前为止，您必须用鼠标来做这件事，但现在不用愁了。 虽然花了六年半的时间，但现在您可以通过按菜单中的“退出游戏”来退出游戏（它取代了 UPLAY 按钮，老实说，没人用那个）。 这不是一个DLL模组！ 这意味着移除DLL文件不会撤销此模组的更改，您将需要恢复您的 cache.psarc 文件备份或验证您的Steam文件。
* **启用直连模式 (Enable Direct Connect Mode)** - **仅限GUI** - https://youtu.be/H6nAB5ogfeU
 * 这个模组启用了一个育碧制作但出于未知原因在发布时禁用的隐藏输入模式。
它基本上是麦克风模式 - 但启用了音色模拟。 这不是一个DLL模组！
这意味着移除DLL文件不会撤销此模组的更改，您将需要恢复您的 cache.psarc 文件备份或验证您的Steam文件。
** 已知问题；某些音频接口报告的吉他输入通道不是游戏所期望的，在这种情况下 - 直连模式可能对您不太适用。
如果您想在应用前测试 - 进入麦克风模式，看看您的接口是否能让您进行一些音符检测。
如果可以 - 那么启用后，直连模式应该能为您工作。
* **更改默认音色 (Change Default tones)** - **仅限GUI**
 * 将您最喜欢的音色添加到音色条的1号槽位。
这是游戏加载时应用的默认音色。
主音、节奏和贝斯都有单独保存的默认音色。
您需要在您的个人资料中保存一个音色。
它不需要被分配到“音色条”槽位，GUI 就能加载它并将其设置为新的默认音色。
这不是一个DLL模组！ 这意味着移除DLL文件不会撤销此模组的更改，您将需要恢复您的 cache.psarc 文件备份或验证您的Steam文件。
* 注意：虽然更改模拟贝斯音色的功能可用且可以轻松添加，但我们不希望编辑此音色，也不赞同任何人编辑此音色。
模拟贝斯音色有一个独特的特性，即无论是在歌曲中还是在菜单中，它始终是相同的音色。
因此，我们认为默认音色很可能是用于各种歌曲/流派的最佳选择。
* **更改默认吉他游乐场音色 (Change Default Guitarcade tones)** - **仅限GUI**
 * 如果您实在无法忍受吉他游乐场游戏中的音色，您可以在这里更改它们。
这不是一个DLL模组！ 这意味着移除DLL文件不会撤销此模组的更改，您将需要恢复您的 cache.psarc 文件备份或验证您的Steam文件。
* **备份玩家资料 (Backup Players Profile)** - **仅限GUI**
 * 每次打开 RSMods GUI 时，它都会备份您的 Rocksmith 玩家资料。
这是一个自动化过程，旨在帮助从资料损坏中恢复。 资料备份可以在 "Rocksmith2014/Profile_Backups/月-日-年_时-分-秒" 文件夹中找到。
## 安装：
* 这个模组有两种安装方式：
1. 手动构建/复制 DLL 文件到 Rocksmith 2014 RM 的根目录，创建一个名为 RSMods.ini 的文件，并按照[下方所示](https://github.com/Lovrom8/RSMods#settings)填写选项。
  如果游戏安装在最常见的文件夹（C盘，Program Files/Steam/Steamapps），Visual Studio 会为了您的方便尝试将 DLL 文件复制到该文件夹。
2. 使用一键安装程序将 DLL 和 RSMods GUI 都复制到游戏文件夹。
如果它无法自动检测 Rocksmith 的安装位置，它会要求您指向正确的文件夹。
## 要求：
* Windows 上最新 Steam 版本的 Rocksmith 2014 Remastered，https://store.steampowered.com/app/221680/Rocksmith_2014_Edition__Remastered/
* DLL 需要 MS Visual C++ 2015-2019 Redistributable，GUI/一键安装程序需要 .NET framework
* 抱歉 Mac 用户，Mac 上的 RS 完全是另一回事，所以我们只支持 Windows 版本。
 
## 依赖项：
* DirectX 9 SDK、ImGUI、GDI+、Detours、RtMidi - 所有这些都包含在项目文件夹中，编译和使用项目应该不需要额外安装。
* 项目设置为 C++17 / VS2019

## 设置：
如果您想手动为 DLL 创建设置文件，请从[这里](https://pastebin.com/raw/f6hf990R)下载模板：

常规文件结构应如下所示： 

| 段落 | 条目 | 可能的值 | 说明 |
| --- | --- | --- | --- |
| **SongListTitles** | | | 
| SongListTitles_1 | _用户定义的字符串_ | 歌曲列表1的名称 | 
| ... | | |
| SongListTitles_6 | _用户定义的字符串_ | 歌曲列表6的名称 | 
| **Keybinds** | | | | 
| ToggleLoftKey | 功能键 (F1, F10) / 媒体键 (播放/暂停, 停止, 下一曲, 上一曲) 的虚拟键码格式。 | 按下此键切换游戏背景。仅当开关设置 > ToggleLoft 开启时可用。 | 
| ShowSongTimerKey | 功能键 (F1, F10) / 媒体键 (播放/暂停, 停止, 下一曲, 上一曲) 的虚拟键码格式。 | 显示正在播放歌曲的当前时间。仅当开关设置 > ShowSongTimer 开启时可用。 | 
| ForceReEnumerationKey | 功能键 (F1, F10) / 媒体键 (播放/暂停, 停止, 下一曲, 上一曲) 的虚拟键码格式。 | 强制游戏检查添加到 DLC 文件夹的新歌曲。 | 
| | | 仅当开关设置 > ForceReEnumeration 开启时可用。 | 
| RainbowStringsKey | 功能键 (F1, F10) / 媒体键 (播放/暂停, 停止, 下一曲, 上一曲) 的虚拟键码格式。 | 让您的琴弦滚动显示颜色。 | 
| | | 仅当开关设置 > RainbowStrings 开启时可用。 | 
| RainbowNotesKey | 功能键 (F1, F10) / 媒体键 (播放/暂停, 停止, 下一曲, 上一曲) 的虚拟键码格式。 | 让您的音符滚动显示颜色。 | 
| | | 仅当开关设置 > RainbowNotes 开启时可用。 | 
| RemoveLyricsKey | 功能键 (F1, F10) / 媒体键 (播放/暂停, 停止, 下一曲, 上一曲) 的虚拟键码格式。 | 在歌曲中切换歌词显示。 | 
| | | 仅当开关设置 > Lyrics 开启时可用。 | 
| RRSpeedKey | 功能键 (F1, F10) / 媒体键 (播放/暂停, 停止, 下一曲, 上一曲) 的虚拟键码格式。 | 使 Riff Repeater 速度超过100%。 | 
| | | 按此键可按“模组设置 > RRSpeedInterval”中的数值增加速度，按住 Shift 再按此键可按该数值减少速度。 |
| | | 仅当开关设置 > RRSpeedAboveOneHundred 开启时可用。 | 
| **Audio Keybindings** | | | |
| MasterVolumeKey | 功能键 (F1, F10) / 媒体键 (播放/暂停, 停止, 下一曲, 上一曲) 的虚拟键码格式。 | 按“模组设置 > VolumeControlInterval”中的数值增加主音量。 | 
| | | 同时按住 Control 和此键可按该数值减小音量。 | 
| | | 仅当开关设置 > VolumeControl 开启时可用。这些值不会在混音器菜单中反映出来。 | 
| | | 这是育碧留下的一个值，但从未在混音器菜单中使用。 | 
| SongVolumeKey | 功能键 (F1, F10) / 媒体键 (播放/暂停, 停止, 下一曲, 上一曲) 的虚拟键码格式。 | 按“模组设置 > VolumeControlInterval”中的数值增加主音量。 | 
| | | 同时按住 Control 和此键可按该数值减小音量。 | 
| | | 仅当开关设置 > VolumeControl 开启时可用。这些值不会在混音器菜单中反映出来。 | 
| Player1VolumeKey | 功能键 (F1, F10) / 媒体键 (播放/暂停, 停止, 下一曲, 上一曲) 的虚拟键码格式。 | 按“模组设置 > VolumeControlInterval”中的数值增加玩家1的音量。 | 
| | | 同时按住 Control 和此键可按该数值减小音量。 |
| | | 仅当开关设置 > VolumeControl 开启时可用。这些值不会在混音器菜单中反映出来。 | 
| Player2VolumeKey | 功能键 (F1, F10) / 媒体键 (播放/暂停, 停止, 下一曲, 上一曲) 的虚拟键码格式。 | 按“模组设置 > VolumeControlInterval”中的数值增加玩家2的音量。 | 
| | | 同时按住 Control 和此键可按该数值减小音量。 | 
| | | 仅当开关设置 > VolumeControl 开启时可用。这些值不会在混音器菜单中反映出来。 | 
| MicrophoneVolumeKey | 功能键 (F1, F10) / 媒体键 (播放/暂停, 停止, 下一曲, 上一曲) 的虚拟键码格式。 | 按“模组设置 > VolumeControlInterval”中的数值增加麦克风音量。 | 
| | | 同时按住 Control 和此键可按该数值减小音量。 | 
| | | 仅当开关设置 > VolumeControl 开启时可用。这些值不会在混音器菜单中反映出来。 | 
| VoiceOverVolumeKey | 功能键 (F1, F10) / 媒体键 (播放/暂停, 停止, 下一曲, 上一曲) 的虚拟键码格式。 | 按“模组设置 > VolumeControlInterval”中的数值增加旁白（Rocksmith之父）音量。 | 
| | | 同时按住 Control 和此键可按该数值减小音量。 | 
| | | 仅当开关设置 > VolumeControl 开启时可用。这些值不会在混音器菜单中反映出来。 | 
| SFXVolumeKey | 功能键 (F1, F10) / 媒体键 (播放/暂停, 停止, 下一曲, 上一曲) 的虚拟键码格式。 | 按“模组设置 > VolumeControlInterval”中的数值增加音效音量。 | 
| | | 同时按住 Control 和此键可按该数值减小音量。 |
| | | 仅当开关设置 > VolumeControl 开启时可用。这些值不会在混音器菜单中反映出来。 | 
| ChangedSelectedVolumeKey | 功能键 (F1, F10) / 媒体键 (播放/暂停, 停止, 下一曲, 上一曲) 的虚拟键码格式。 | 显示所选音量的当前值。 | 
| ToggleExtendedRangeKey | 功能键 (F1, F10) / 媒体键 (播放/暂停, 停止, 下一曲, 上一曲) 的虚拟键码格式。 | 切换扩展音域模式。 | 
| **Toggle Switches** | | | | 
| ToggleLoft | on/off | 关闭游戏背景。 | 
| | | 这将使背景变为黑色。 | 
| VolumeControl | on/off | 允许您通过按键绑定来更改音量。 | 
| ShowSongTimer | on/off | 显示您正在播放的歌曲的时间。 | 
| ForceReEnumeration | automatic/manual | 强制游戏查找添加到您DLC文件夹中的新歌曲。 | 
| RainbowStrings | on/off | 使您的琴弦在一个色轮中循环显示。 | 
| RainbowNotes | on/off | 使您的音符在一个色轮中循环显示。 | 
| ExtendedRange | on/off | 根据歌曲的调音更改您的琴弦颜色。 | 
| | | 这对于使用7弦吉他或5弦贝斯演奏低调音歌曲的人很有帮助。 | 
| ExtendedRangeDropTuning | on/off | ExtendedRange的扩展，使降调调弦也会触发颜色变化。 | 
| CustomStringColors | 0/1/2 | 0 = 默认颜色, 1 = ZZ的颜色集, 2 = 在“琴弦颜色”部分指定的颜色 | 
| Headstock | on/off | 移除琴头，呈现“无头吉他”的外观。 | 
| Skyline | on/off | 从屏幕顶部移除紫色和橙色的动态难度条，以获得更简洁的用户界面。 | 
| GreenScreenWall | on/off | 移除背景墙的纹理，如果您想要“切换背景”模式的外观但仍希望音箱/背景元素显示出来。 | 
| ForceProfileLoad | on/off | 游戏启动时连续按回车键，这样您就可以去冲杯咖啡，回来时已经进入主菜单了。 | 
| Fretless | on/off | 从吉他/贝斯模型中移除品丝。 | 
| Inlays | on/off | 从吉他/贝斯上移除品记。 | **仅适用于标准圆点品记** |
| ToggleLoftWhen | startup/song/manual | 您希望“切换背景”在何时生效？ | 
| LaneMarkers | on/off | 移除您当前未使用通道上过多的沿音轨向下的线条。 | 
| ToggleSkylineWhen | startup/song | 您希望“天际线”在何时被移除？ | 
| Lyrics | on/off | 从游戏中移除歌词以获得更简洁的用户界面。 | 
| RemoveLyricsWhen | startup/manual | 您希望“歌词”在何时被移除？ | 
| GuitarSpeak | on/off | 允许弹奏的音符触发按键，这样您就可以把键盘放在一边，只用您的吉他/贝斯来控制用户界面。 | 
| | | 触发按键的音符在“吉他语音控制”部分定义。 | 
| RemoveHeadstockWhen | startup/song | 您希望“琴头”在何时被移除？ | 
| ScreenShotScores | on/off | 在您完成一首歌时进行Steam截图。 | 需要Steam的截图键设置为F12。 | 
| RRSpeedAboveOneHundred | on/off | 移除Riff Repeater的100%速度限制，以比预期更快的速度播放歌曲。 | 
| AutoTuneForSong | on/off | 如果您拥有我们支持的几款踏板之一，我们可以向踏板发送信号以启用降调功能，从而减少歌曲之间的切换时间。 | 
| | | 我们使用MIDI发送信号。支持的踏板可以在本页底部的问答部分看到。 | 
| ChordsMode | on/off | “自动为歌曲调音”的扩展功能，其中一些踏板有两种独立的演奏模式。 | 这使我们能够根据您在踏板上的设置发送正确的信号。 | 
| ShowCurrentNoteOnScreen | on/off | 读取当前正在弹奏的音符并将其显示在屏幕上。 | 
| | | 这仅适用于单音，因此和弦将**无法**正常工作。 | 
| OnScreenFont | _font_name_ | 当我们需要在屏幕上向您显示文本时使用的字体名称。 | 
| | | 如果我们找不到您指定的字体，则默认为Arial。 |
| ProfileToLoad | _profile_name_ | “强制加载配置文件”的扩展功能，我们将在所有配置文件的列表中查找您指定的配置文件。 | 
| | | 如果您有多个配置文件，或者有多个用户在同一台计算机上玩，这将很有帮助。 | 
| ShowSongTimerWhen | automatic/manual | 您希望“歌曲计时器”在何时显示？ | 
| SecondaryMonitor | on/off | 启动Rocksmith并自动将其移动到另一台显示器。 | 
| **String Colors** | | 十六进制定义的颜色 (例如 FF0000) | | 
| string0_N | | 用于非扩展音域歌曲的琴弦颜色 | 
| ... | | |
| string5_N | | | 
| string0_CB | | 用于扩展音域歌曲的琴弦颜色 | 
| ... | | |
| string5_CB | | | 
| note0_N | | 用于非扩展音域歌曲的音符颜色 | 
| ... | | |
| note5_N | | | 
| note0_CB | | 用于扩展音域歌曲的音符颜色 | 
| ... | | |
| note5_CB | | | 
| **Mod Settings** | | | |
| ExtendedRangeModeAt | 数值 | 相对于E标准的偏移量 (-1 = Eb, -5 = B) | 
| CheckForNewSongsInterval | 毫秒为单位的时间间隔 | 每次枚举检查之间的时间 | 
| RRSpeedInterval | 数值 | 按下RRSpeedKey时速度增加/减少的百分比 | 
| TuningPedal | 数值 | 您拥有的踏板编号。0 = 关闭, 1 = Whammy DT, 2 = Bass Whammy, 3 = Whammy | 
| TuningOffset | 数值 | “ExtendedRangeModeAt”的偏移量，显示您的吉他距离E标准**调音**有多远。(-1 = Eb, -5 = B) | 
| VolumeControlInterval | 数值 | 当您按下音频键绑定时，音量上升/下降的百分比。 | 
| SecondaryMonitorXPosition | 数值 | 第二显示器左上角的X坐标（虚拟屏幕） | 
| SecondaryMonitorYPosition | 数值 | 第二显示器左上角的Y坐标（虚拟屏幕） | 
| SeparateNoteColors | 数值 | 0 = 使用与琴弦相同的颜色, 1 = 正常RS颜色, 2 = 自定义音符颜色 | 
| **Guitar Speak** | | | | 
| GuitarSpeakDeleteWhen | 数值 | 将触发按下Delete键的Midi音符。 | 
| GuitarSpeakSpaceWhen | 数值 | 将触发按下Space键的Midi音符。 | 
| GuitarSpeakEnterWhen | 数值 | 将触发按下Enter/Return键的Midi音符。 | 
| GuitarSpeakTabWhen | 数值 | 将触发按下Tab键的Midi音符。 | 
| GuitarSpeakPGUPWhen | 数值 | 将触发按下Page Up键的Midi音符。 | 
| GuitarSpeakPGDNWhen | 数值 | 将触发按下Page Down键的Midi音符。 | 
| GuitarSpeakUPWhen | 数值 | 将触发按下Up Arrow键的Midi音符。 |
| GuitarSpeanDNWhen | 数值 | 将触发按下Down Arrow键的Midi音符。 | 
| GuitarSpeakESCWhen | 数值 | 将触发按下Escape键的Midi音符。 | 
| GuitarSpeakCloseWhen | 数值 | 将触发停止Guitar Speak的Midi音符。 | 
| GuitarSpeakOBracketWhen | 数值 | 将触发按下左方括号 [ 键的Midi音符。 | 
| GuitarSpeakCBracketWhen | 数值 | 将触发按下右方括号 ] 键的Midi音符。 | 
| GuitarSpeakTildeaWhen | 数值 | 将触发按下波浪号~键的Midi音符。 | 
| GuitarSpeakForSlashWhen | 数值 | 将触发按下正斜杠/键的Midi音符。 | 
| GuitarSpeakAltWhen | 数值 | 将触发按下Alt键的Midi音符。 | 
| GuitarSpeakWhileTuning | on/off | 在调音时是否启用GuitarSpeak（仅限高级用户） | 
| **Highway Colors** | | | |
| CustomHighwayColors | on/off | 我们是否应该使用自定义的音符公路？ | 
| CustomHighwayNumbered | 十六进制定义的颜色 (例如 FF0000) | | 
| CustomHighwayUnNumbered | 十六进制定义的颜色 (例如 FF0000) | |
| CustomHighwayGutter | 十六进制定义的颜色 (例如 FF0000) | | 
| CustomFretNubmers | 十六进制定义的颜色 (例如 FF0000) | | 
| **GUI Settings** | | | |
| CustomTheme | on/off | GUI的自定义颜色 | 
| ThemeBackgroundColor | 十六进制定义的颜色 (例如 FF0000) | 背景颜色 | 
| ThemeTextColor | 十六进制定义的颜色 (例如 FF0000) | 文本颜色 | 
| ThemeButtonColor | 十六进制定义的颜色 (例如 FF0000) | 按钮颜色 | 
| BackupProfile | on/off | 创建您的Rocksmith个人资料/存档的备份，以防万一它被损坏。 | 
| NumberOfBackups | 数值 | 我们应该存储多少个备份？ |
* 键绑定部分可用的键可以在这里看到：![视觉表示](https://i.imgur.com/lpNv3yG.png) 您必须遵循此处提供的V-Key格式：https://docs.microsoft.com/en-us/windows/win32/inputdev/virtual-key-codes（是的，包括VK_部分）。 
例如，F3将是VK_F3，音乐播放/暂停按钮将是VK_MEDIA_PLAY_PAUSE。 
我们理解我们限制键的数量可能会激怒你们中的一些人，但我们希望让您在搜索歌曲时不必在搜索“Slipknot”时打开/关闭您的模组。 
**如果您是主播并且有Elgato Stream Deck**，请将您的键绑定设置为F13-F24键，因为大多数键盘没有这些键，但我们允许它们用于键绑定。 
* 琴弦编号从0-5，因为这是零索引的，或者说计算机通常的工作方式。 
转换过来就是：0. 低E弦，1. A弦，2. D弦，3. G弦，4. B弦，5. 高E弦。 

* Guitar Speak的音符值从C-1到C6测量，从0开始到96。 例如，第12品的低E弦是E3，将转换为数字52。 

* GuitarSpeakWhileTuning仅适用于高级用户，因为如果它开启并且您的GuitarSpeak值设置错误，它可能会阻止您调音或玩这个游戏。 
做出这个决定是为了防止人们因为GuitarSpeak阻止他们摇滚而卸载这个模组。 
* 歌曲列表名称应少于25个字符（包括空格），因为文本会拉伸并变得难以阅读。 
## FAQ

* 问：我如何设置我的直播流，使其透明/黑色等？
* 答： 

  0. 从发布页面下载RSMods，运行安装程序，然后单击按钮安装模组。
  1. 进入“启用/禁用模组”选项卡。 
  2. 勾选名为“切换背景”的复选框。
  3. 进入“禁用UI元素”子选项卡。 
  4. 在“何时关闭背景”部分，将其设置为“始终”。 
这将使您的游戏始终具有黑色背景（在您进入游戏后，不包括个人资料屏幕/登录屏幕等）。 
5. 在您的OBS / SLOBS中，您需要设置一个抠像。 
在OBS中是Luma Key（亮度抠像），在SLOBS中是Color key（颜色抠像）。 
如果您不想 messing with 任何其他模组，可以关闭RSMods。 
OBS：
  1. 右键单击您的捕获源，然后单击“滤镜”。 
2. 单击“+”按钮，选择“亮度抠像 (Luma Key)”，然后点击“确定”。 
3. 除了“Luma Max”应为1.00外，其他所有选项都保持0.00。
  4. 点击关闭以保存您的更改。
5. 添加一个背景，这样默认就不会只是黑色。 
对我来说，我只是画了一张快速的图像，并将其放在游戏下面。 
* 结果：https://i.imgur.com/MX5GQNU.png

  SLOBS：
  1. 右键单击您的捕获源，然后单击“滤镜”。 
2. 点击“+”按钮，选择“颜色抠像 (Color Key)”，给它取任何您想要的名字，然后点击“完成”。 
3. 在“Key Color Type”中选择“自定义颜色”，点击新的“Key Color”框并将其拖到左下角。 
如果操作正确，它应该显示“#00000000”。 
  4. 将“相似度”设置为1。
  5. 将“平滑度”设置为150，其他所有选项保持默认，然后点击“完成”。
6. 添加一个背景，这样默认就不会只是黑色。 
对我来说，我只是画了一张快速的图像，并将其放在游戏下面。 
* 结果：https://cdn.discordapp.com/attachments/758715497352396860/822917699088154664/unknown.png

* 问：哪些踏板可以通过MIDI自动调音？
* 答：目前支持自动降调的踏板是Digitech Whammy DT、Digitech Whammy和Digitech Bass Whammy。 
感谢PoizenJam为让后两款踏板按预期工作所做的努力。 
* 问：我希望向模组添加一些东西，比如我想从游戏中移除XYZ！！！ 
* 答：请在此Github仓库的[Issues选项卡](https://github.com/Lovrom8/RSMods/issues)中以“DLL - FR - XYZ”的标题发布请求。 
请遵循此格式，以便我们知道我们是在做什么，是修复问题还是添加新功能。 
注意：仅仅因为您发布了一个请求，并不意味着我们能够做到和/或我们会去做。 
请不要一直恳求我们处理您的请求，如果我们认为这值得我们花时间，我们会去处理的。 
* 问：我发现了一个bug/有些东西工作不正常！我该如何解决？
* 答：如果bug在Rocksmith中，请在此Github仓库的[Issues选项卡](https://github.com/Lovrom8/RSMods/issues)中以“DLL - Bug - XYZ”的标题发布问题；如果bug在修改游戏的工具中，则以“GUI - Bug - XYZ”为标题。 
请尽量描述清楚，因为发布“它不工作”对我们没有帮助。 
截图和/或视频可以提供帮助，但您是如何让它出问题的步骤将不胜感激。 
有时bug是我们获得最佳功能的地方 :) 


* 问：这些模组是谁制作的，我该如何感谢你们？
* 答：感谢您对该项目表现出兴趣。 
我们花了十多个月的时间来充实这个项目，以便人们会喜欢使用它。 
开发人员主要是：LovroM8 (Lovro) 和 Ffio1 (Ffio)，但我们也得到了 ZagatoZee (ZZ)、Kokolihapihvi (Koko) 和 L0fka 的大量帮助。 
我们只求一声简单的感谢，您可以通过在Github上给这个项目加星、告诉您的Rocksmith朋友，或者只是来Discord说声“谢谢”来表达。 
我知道这听起来不多，但它真的能让我们开心一整天（甚至好几天）。 
* 如果您有任何问题，欢迎随时在[r/Rocksmith Discord](https://rocksmith.rocks/discord)的#rsmods频道中与我们联系。