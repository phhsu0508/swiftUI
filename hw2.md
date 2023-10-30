<h1>hw2</h1>
<table>
    <tr>
        <td>
            <img src="https://raw.githubusercontent.com/phhsu0508/swiftUI/main/hw2demo.jpg">
                </td>        
 <td>

  
```swift
import SwiftUI
struct ContentView: View {
    var body: some View {
    
        ZStack{
            Image("bg")
                .resizable()
                .scaledToFill()
                .opacity(0.3)
            VStack {
                TitleView()
                
                HStack{
                    PICView(pic: "one", Name: "Vol.1")
                    PICView(pic: "two", Name: "Vol.2")
                    PICView(pic:"three", Name: "Vol.3")
                }
                HStack{
                    PICView(pic: "four", Name: "Vol.4")
                    PICView(pic: "five", Name: "Vol.5")
                    PICView(pic: "six", Name: "Vol.6")
                }
                TitleView2()
                HStack{
                    PICView(pic: "G1", Name: "壓克力立牌")
                    PICView(pic: "G2", Name: "透明資料夾")
                    PICView(pic: "G3", Name: "手提袋")
                }
                
            }
        }
        
} 
    
}

struct TitleView: View { var body: some View {
    VStack(alignment:.center, spacing:2){ 
        Text("Bluray & DVD")
            .font(.system(size:25)) 
            .foregroundColor(.blue)
        
    }
}
}

struct TitleView2: View { var body: some View {
    VStack(alignment:.center, spacing:2){ 
        Text("\nGoods")
            .font(.system(size:25)) 
            .foregroundColor(.blue)
        
    }
}
}

struct PICView: View { 
    var pic:String
    var Name:String
    var body: some View {
    VStack{
        Image(pic)
            .resizable() 
            .aspectRatio(contentMode:.fit)
            .frame(width:128, height:160,
                   alignment: .top)
            //.scaledToFill()
            .padding(.all, 2)
        Text(Name) 
            .fontWeight(.bold) 
            .font(.system(size: 15))
    } 
    
}
}
```
</td>
</tr>
</table>
