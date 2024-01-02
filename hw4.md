<h1>hw4</h1>
<table>
    <tr>
        <td>
            <img src="https://raw.githubusercontent.com/phhsu0508/swiftUI/main/hw4demo.gif">
                </td>        
 <td>

 
```swift
import SwiftUI
struct ContentView: View { 
    
    var body: some View {
            VStack{ 
                Image("anime")
                    .resizable()
                    .scaledToFit()
                TabView{
                    HomeView()
                        .tabItem {
                            Image(systemName: "homekit")
                            Text("Home")
                        }
                    ListView()
                        .tabItem {
                            Image(systemName: "list.dash")
                            Text("Goods")
                        }
                    BookView()
                        .tabItem {
                            Image(systemName: "tv")
                            Text("Story")
                        }
                }
                
            }
        
    }
}

struct HomeView: View{
    var body: some View{
        ZStack{
            Image("bg2")
                .resizable()
                .scaledToFill()
                
        }
    }
}

struct Dvd:Identifiable {
var id = UUID()
var name:String
var image:String
var content:String
var description:String
}
var dvds = [ Dvd(name: "vol.1",image: "one", content:"d1",  description:"【Blu-ray】\n品番：KAXA-8601　価格：￥9,900（税込）\n【DVD】\n品番：KABA-11371　価格：￥8,800（税込）\n収録内容：第１話＋特典映像\n\n初回生産特典\n1.キャラクターデザイン・平山寛菜描き下ろしデジパック\n2.スペシャルケース\n3.スペシャルブックレット\n4.特製リーフレット\n【推しの子】Mother and Children入場者プレゼント：\nキャラクターデザイン・平山寛菜描き下ろしミニ色紙イラスト全4種を再録\n5.絵コンテ集\n\n每回特典\n1.映像特典：【OSHI NO KO】Behind the Scenes Ep1\n2.オーディオコメンタリー （第一話：高橋李依、伊東健人、伊駒ゆりえ、内山夕実）\n3.PV"),
             Dvd(name: "vol.2",image: "two", content:"d2", description:"【Blu-ray】\n品番：KAXA-8602　価格：￥7,700（税込）\n【DVD】\n品番：KABA-11372　価格：￥6,600（税込）\n収録内容：第２話～第３話＋特典映像\n\n初回生産特典\n1.キャラクターデザイン・平山寛菜\n描き下ろしデジパック\n2.スペシャルケース\n3.スペシャルブックレット\n\n每回特典\n1.映像特典：\n【OSHI NO KO】Behind the Scenes Ep2\n2.オーディオコメンタリー \n（第三話：大塚剛央、伊駒ゆりえ、潘めぐみ）\n3.PV\n4.WEB予告（第二話・第三話）"),
             Dvd(name: "vol.3",image: "three", content:"d3", description:"【Blu-ray】\n品番：KAXA-8603　価格：￥7,700（税込）\n【DVD】\n品番：KABA-11373　価格：￥6,600（税込）\n収録内容：第４話～第５話＋特典映像\n\n初回生産特典\n1.キャラクターデザイン・平山寛菜\n描き下ろしデジパック\n2.スペシャルケース\n3.スペシャルブックレット\n\n每回特典\n1.映像特典：\n【OSHI NO KO】Behind the Scenes Ep3\n2.オーディオコメンタリー \n（第五話：大塚剛央、伊駒ゆりえ、村田太志）\n3.ノンクレジットオープニング\n4.WEB予告（第四話・第五話）"),
             Dvd(name: "vol.4",image: "four", content:"d4", description:"【Blu-ray】\n品番：KAXA-8604　価格：￥7,700（税込）\n【DVD】\n品番：KABA-11374　価格：￥6,600（税込）\n収録内容：第６話～第７話＋特典映像\n\n初回生産特典\n1.キャラクターデザイン・平山寛菜\n描き下ろしデジパック\n2.スペシャルケース\n3.スペシャルブックレット\n\n每回特典\n1.映像特典：\n【OSHI NO KO】Behind the Scenes Ep4\n2.オーディオコメンタリー \n（第七話：大塚剛央、石見舞菜香、大久保瑠美）\n3.ノンクレジットオープニング\n4.WEB予告（第六話・第七話）"),
             Dvd(name: "vol.5",image: "five",content:"d5",  description:"【Blu-ray】\n品番：KAXA-8605　価格：￥7,700（税込）\n【DVD】\n品番：KABA-11375　価格：￥6,600（税込）\n収録内容：第８話～第９話＋特典映像\n\n初回生産特典\n1.キャラクターデザイン・平山寛菜\n描き下ろしデジパック\n2.スペシャルケース\n3.スペシャルブックレット\n\n每回特典\n1.映像特典：\n【OSHI NO KO】Behind the Scenes Ep5\n2.オーディオコメンタリー \n（第九話：伊駒ゆりえ、潘めぐみ、大久保瑠美）\n3.番宣\n4.WEB予告（第八話・第九話）"),
             Dvd(name: "vol.6",image: "six", content:"d6", description:"【Blu-ray】\n品番：KAXA-8606　価格：￥7,700（税込）\n【DVD】\n品番：KABA-11376　価格：￥6,600（税込）\n収録内容：第10話～第11話＋特典映像\n\n初回生産特典\n1.キャラクターデザイン・平山寛菜\n描き下ろしデジパック\n2.スペシャルケース\n3.スペシャルブックレット\n\n每回特典\n1.映像特典：\n【OSHI NO KO】Behind the Scenes Ep6\n2.オーディオコメンタリー \n（第十一話：大塚剛央、伊駒ゆりえ、潘めぐみ、大久保瑠美）\n3.CM\n4.WEB予告（第十話・第十一話）")
]

struct ImageRow: View{
    var thisdvd: Dvd
    var body: some View{
        HStack{
            Image(thisdvd.image)
                .resizable()
                .frame(width: 40, height:40)
                .cornerRadius(5)
            Text(thisdvd.name)
        }
    }
}

struct DetailView: View{
    @Environment(\.presentationMode) var presentationMode
    var thisdvd: Dvd
var body: some View{
            ScrollView() {
                VStack{
                    Image(thisdvd.content)
                        .resizable()
                        .aspectRatio(contentMode: .fit)
                        .clipped()
                    Text(thisdvd.name)
                        .font(.system(.title, design:.rounded))
                        .fontWeight(.black)
                    Text(thisdvd.description)
                        .font(.system(.subheadline, design:.rounded))
                        .fontWeight(.black)
                    Spacer()
                }
            }.overlay(
                HStack{
                    Spacer()
                    VStack{
                        Button(action:{
                            self.presentationMode.wrappedValue.dismiss()},label:{
                                Image(systemName: "chevron.down.circle.fill")
                                    .foregroundColor(.gray)
                            
                        })
                        .padding(.trailing, 20)
                        .padding(.top, 40)
                        Spacer()
                    }
                })

        
    }
}
struct ListView: View{
    @State var showDetailView = false
    @State var selecteddvd:Dvd?
    var body: some View{
        
        NavigationView{
            List(dvds){ dvdItem in 
                ImageRow(thisdvd: dvdItem)
                    .onTapGesture{
                        self.showDetailView = true
                        self.selecteddvd = dvdItem
                    }
            }
            .sheet(item:self.$selecteddvd){
                thisdvd in DetailView(thisdvd: thisdvd)
            }
            .navigationBarTitle("Blu-ray & DVD")
        }
    }
}
struct TermAndDescription: Identifiable{ var id = UUID()
    var term:String
    var title:String
    var description:String }
var myDictionary = [
    TermAndDescription(term: "第一話", title: "Mother and Children", description: "産婦人科医・ゴローの前に現れた患者は、推しのアイドル・アイだった。ショックを受けながらも医者として彼女を支えるゴロー。だが出産直前、ゴローは何者かに襲われ…！？"),TermAndDescription(term: "第二話", title: "三つ目の選択肢", description: "アイの死から十数年。遺された双子の妹・ルビーはアイドルを目指すが、兄・アクアの根回しによってチャンスを掴めずにいた。だが母に憧れるルビーの気持ちは止まらず…。"),TermAndDescription(term: "第三話", title: "漫画原作ドラマ", description: "元天才子役・かなと再会したアクア。ドラマ出演の打診をすげなく断るが、プロデューサーの名前を聞くなり返事を翻す。その名はアイの携帯電話に残されたものと同じで…！？"),TermAndDescription(term: "第四話", title: "役者", description: "作品を少しでも良くしようと懸命に演じるかな。だが主演の酷い芝居や、それを是とする監督達に失望が募る。そんな中、アクアの演技が現場を一変させる…！"),TermAndDescription(term: "第五話", title: "恋愛リアリティショー", description: "一刻も早くアイドル活動を始めたいルビーは、かなをスカウト。ルビーに可能性を感じつつも、かなはリスクを鑑みて断ろうとする。だがアクアに熱烈に口説き落とされ……！？"),TermAndDescription(term: "第六話", title: "エゴサーチ", description: "『今ガチ』の収録が進む中、女優・あかねは爪痕を残せずにいた。目立ちたい一心でヒールのように振る舞うも、望む反響は得られない。焦りを募らせたあかねは…！？"),TermAndDescription(term: "第七話", title: "バズ", description: "歩道橋の欄干に立ったあかねを引きずり戻したアクア。共演者に支えられ彼女は番組を続ける決意をする。一方アクアは、あかねに染み付いた偏見を払拭する為の策を実行する！"),TermAndDescription(term: "第八話", title: "初めて", description: "完璧にアイを理解し、行動をトレースしてみせるあかね。さらに彼女は、アイに隠し子がいたことまで見抜いていた。女優・あかねに強い興味を抱いたアクアは…！？"),TermAndDescription(term: "第九話", title: "B小町", description: "元々アイドルを夢見ていたというＭＥＭちょ。人気も知名度も高く、契約上の問題もない。Ｂ小町の新メンバーとして申し分のない彼女だが、とある秘密を抱えていて…！？"),TermAndDescription(term: "第十話", title: "プレッシャー", description: "ジャパンアイドルフェス出演決定！そんなＢ小町に立ちはだかる『センターを誰にするか』問題。ルビーとＭＥＭちょは、歌が上手いかなをセンターにしようと画策するが…！？"),TermAndDescription(term: "第十一話", title: "アイドル", description: "ついにステージに立ったＢ小町。ＭＥＭちょ目当ての客が詰めかける中、ルビーは亡きアイを思わせる笑顔で観客を魅了する。だが、かなを応援するサイリウムの光はなく…。")
]

struct BookView: View{
    @State var currentCard = 0
    var body: some View{
        VStack{
            VStack{
                Text(myDictionary[currentCard].term) 
                    .padding(.all, 10)
                    .foregroundColor(.white)
                    .fontWeight(.heavy)
                    .font(.system(size: 20))
                    .frame(width:110, height:30, alignment: .center)
                    .background(Color.pink)
                    .opacity(0.9)
                Text(myDictionary[currentCard].title) 
                    .font(.system(size: 24))
                    .padding()
                    //.frame(width:300, height:30, alignment: .center)
                    //.background(Color.gray.opacity(0.5))
                Text(myDictionary[currentCard].description)
                    .font(.body) 
                    .foregroundColor(.white) 
                    .padding(.all, 10)
                    .frame(width:250, height:240, alignment: .center)
                    .background(Color.gray.opacity(0.5).padding(10))
                    
                    
                    
        }
        //.frame(minWidth: 0, idealWidth: 100, maxWidth: 300,
          //     minHeight: 0, idealHeight: 100, maxHeight: 300, alignment: .center)
        .background(Image("bg")
            .resizable().aspectRatio(contentMode: .fill).opacity(0.9).blur(radius: 15))
        .onTapGesture { 
            if currentCard<myDictionary.count-1{
                currentCard+=1 }
            else{
                currentCard=0
            }
        }
        Text("Tap to next part")
            .padding(.all, 20)
    }
     }
        
    
}

```
</td>
</tr>
</table>
