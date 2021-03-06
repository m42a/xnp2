
　Neko Project II
                                       NP2 developer team, 1999-2001,2003,2004


・概要

　　PC-9801VX21をベースとして、PC-9801シリーズの主要な機能をソフトウェアで
　　再現するエミュレータです。

　　ねこープロジェクトIIが再現するのは PC-9801シリーズの標準的なハードウェアと
　　一部のBIOSとCバスデバイスのみです。
　　このため、MS-DOS等は動作しますが、N88-BASICやLIO等のROMを使用するものは
　　標準で動作しません。これらを動作させるためには実機より ROMを取得する必要が
　　あります。



・推奨動作環境

　　ARM 206Mhz以上
　　WinCE 2.11以上
　　10MB以上の空きメモリ

　　PocketPC, Sigmarion3では gx.dllが必要です。
　　(PocketPC2002では 最初から導入済みです)



・使用方法

　　ねこープロジェクトIIを使うには フロッピーイメージが必要です。
　　webの情報を基にイメージ化を行なって下さい。

　　その後 np2hpc/np2ppc/np2sig3の機種にあったバイナリを起動します。

　　フロッピーベースのソフトウェアを起動するには、メニューの
　　[FDD1 - Open], [FDD2 - Open]を選択しディスクイメージを挿入した後に
　　リセットしてください。

　　ハードディスクを使用するには [Emulate - Newdisk] より、ハードディスク
　　イメージを作成してから [HardDisk - SASI-1 - Open]よりイメージファイルを
　　選択したのち、リセットしてください。
　　ハードディスクイメージの使用情報は記憶されますので、イメージファイルを
　　変更するしない限りは この操作は必要ありません。

　　CPUは 80286(リアルモードのみ)です。
　　環境を構築する場合、プロテクトモードを扱えない事に注意して下さい。
　　また DIP SW3-8 OFFで V30ぽい動きをするようにしています。
　　CPUスピードは Configureで変更出来ます。

　　実行し、設定を変えると np2.cfgファイルが作成されます。



・メニュー

　　Emulate
　　　Reset                     ハードウェアリセットします。
　　　Configure                 設定を開きます。
　　　Exit                      ねこープロジェクトIIを終了します。

　　FDD1
　　　Open                      ドライブ１のディスクイメージを選択します。
　　　Eject                     ドライブ１のディスクイメージを取出します。

　　FDD2
　　　Open                      ドライブ２のディスクイメージを選択します。
　　　Eject                     ドライブ２のディスクイメージを取出します。

　　HardDisk
　　　SASI-1
　　　　Open                    SASI-1のハードディスクイメージを選択します。
　　　　Remove                  SASI-1を未設続状態に戻します。
　　　SASI-2
　　　　Open                    SASI-2のハードディスクイメージを選択します。
　　　　Remove                  SASI-2を未設続状態に戻します。

　　Screen
　　　Disp Vsync                描画タイミング (チェックでVsync時)
　　　Real Palettes             パレット更新タイミング (チェックでラスタごと)
　　　No Wait                   タイミングを取りません。
　　　Auto frame                表示タイミングを自動的に決定します。
　　　Full frame                全てのフレームを表示します。
　　　1/2 frame                 ２回に１度描画します。
　　　1/3 frame                 ３回に１度描画します。
　　　1/4 frame                 ４回に１度描画します。
　　　Screen option             スクリーン設定を開きます。

　　Device
　　　Keyboard
　　　　Keyboard                テンキーをキーボードとして扱います。
　　　　JoyKey-1                テンキーをジョイスティック１に割り当てます。
　　　　JoyKey-2                テンキーをジョイスティック２に割り当てます。
　　　　MouseKey                テンキーをマウスに割り当てます。
　　　　mechanical SHIFT        ノート風メカニカルシフトにします。
　　　　mechanical CTRL         ノート風メカニカルコントロールにします。
　　　　mechanical GRPH         ノート風メカニカルグラフキーにします。
　　　Sound
　　　　Beep off                ビープを無音にします。
　　　　Beep low                ビープ音量を小にします。
　　　　Beep mid                ビープ音量を中にします。
　　　　Beep high               ビープ音量を大にします。
　　　　Disable boards          FM音源ボードを使用しません。
　　　　PC-9801-14              ミュージックジェネレータボードを使用します。
　　　　PC-9801-26K             PC-9801-26Kボードを使用します。
　　　　PC-9801-86              PC-9801-86ボードを使用します。
　　　　PC-9801-26K + 86        PC-9801-26Kと86ボードを使用します。
　　　　PC-9801-86 + Chibi-oto  PC-9801-86ボードとちびおとを使用します。
　　　　PC-9801-118             PC-9801-118ボードを使用します。
　　　　Speak board             スピークボードを使用します。
　　　　Spark board             スパークボードを使用します。
　　　　AMD-98                  AMD-98を使用します。
　　　　JAST SOUND              JAST SOUNDを使用します。
　　　　Seek Sound              ディスクシークタイミングを取ります。
　　　Memory
　　　　640KB                   メモリをメインメモリのみ使用します。
　　　　1.6MB                   メインメモリと拡張メモリ1MBを使用します。
　　　　3.6MB                   メインメモリと拡張メモリ3MBを使用します。
　　　　7.6MB                   メインメモリと拡張メモリ7MBを使用します。
　　　Mouse                     マウス操作を切替えます。
　　　MIDI panic                MIDIを消音します。



・設定ダイアログ

　　Configue
　　　CPU
　　　　Base Clock              CPUのベースクロックを指定します。
　　　　Multiple                CPUのクロック倍率を指定します。
　　　Architecture
　　　　PC-9801VM               V30以前のCPUを搭載したNEC仕様となります。
　　　　PC-9801VX               i286以降のCPUを搭載したNEC仕様となります。
　　　　PC-286                  EPSON互換機仕様となります。
　　　Sound
　　　　Sampling Rate           サウンドの出力周波数を指定します。
　　　　Buffer                  サウンドのバッファサイズを指定します。
      Resume                    レジューム機能を使用します。

　　Screen option
　　　Video
　　　　LCD                     PC-98ノートの液晶モードになります。
　　　　Reverse                 液晶表示を反転します。
　　　　Use skipline rev        スキップラインを補正します。
　　　　Ratio                   スキップラインの明るさを指定します。
　　　Chip
　　　　GDC                     GDCチップを指定します。
　　　　GRCG                    GRCGチップを指定します。
　　　　Enable 16color          アナログ16色カラーを有効にします。
　　　Timing
　　　　T-RAM                   テキストRAMアクセスウェイト値を指定します。
　　　　V-RAM                   ヴィデオRAMアクセスウェイト値を指定します。
　　　　GRCG                    GRCG使用時のアクセスウェイト値を指定します。
　　　　RealPalettes Adjust     RealPalettes時のタイミングを調整します。



・ディスクイメージ

　　以下にイメージ対応しています。
　　　FDD  - D88形式, XDF(ベタイメージ)形式
　　　SASI - THD形式(T98), HDI形式(Anex86)



・キー設定について
　　bios.romとかと同じフォルダに(機種によって異なるのでこんな書き方…)
　　key.txtという名前でテキストファイルを作成して、キー設定を記入して下さい。

　　書式)
　　　[keyname] = [key1] (key2) (key3)
　　　[keyname] [TAB] [key1] (key2) (key3)
　　　userkey[1-2] = [key1] (key2) (key3) ... (key15)
　　　　フルキー 0〜9 A〜Z - ^ \ @ [ ] ; : , . / _
　　　　         STOP COPY ESC TAB BS RET SPC XFER NFER
                 INS DEL RLUP RLDN HMCL HELP
　　　　ファンク F1〜F10 VF1〜VF5
　　　　テンキー [0]〜[9] [-] [/] [*] [+] [=] [,] [.]
　　　　シフト   SHIFT CAPS KANA GRPH CTRL

　　　通常キーは3個、userkeyは15個の同時押し設定が可能です。
　　　[=] キーは = で区切られてしまうので TABで区切るか [EQU]として下さい。

　　　例:
        ----------------------- key.txt

　　　　W = UP                 (ダイアモンドキーをカーソルにしてみたり…)
　　　　S = LEFT
　　　　D = RIGHT
　　　　X = DOWN
　　　　[7] = [4] [8]          (テンキー斜め同時押しにしてみたり…)
　　　　[9] = [6] [8]
　　　　[1] = [4] [2]
　　　　[3] = [6] [2]
　　　　userkey1 = CTRL XFER   (CTRL+XFER FEP切り替え)
　　　　userkey2 = D O A Z     (D+O+A+Z 同時押し)

        -----------------------



　Windows版と共通点が多いので Windows版ヘルプもご覧ください。
　　http://www.yui.ne.jp/np2/help.html


　　　　　　　　　　　　　　　　　　email: np2@yui.ne.jp
　　　　　　　　　　　　　　　　　　webpage: http://www.yui.ne.jp/np2/
