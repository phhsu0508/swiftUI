<h1>hw1</h1>
<table>
    <tr>
        <td>
            <img src="https://raw.githubusercontent.com/phhsu0508/swiftUI/main/IMG_0775.jpeg">
                </td>        
 <td>

  
```swift
import SwiftUI

struct ContentView: View {
    var body: some View {
        
        Image("bg")
            .resizable()
            .scaledToFill()
            .opacity(0.85)
        
            .overlay(
                Image("Hsu")
                    .resizable()
                    .scaledToFit()
                    .clipShape(Circle(), style: FillStyle())
                    .frame(width: 150, height: 250, alignment: .top)
                
                    .overlay(Text("學號：1103314\n姓名：許博翔")
                        .lineSpacing(10.0)
                        .fontWeight(.medium)
                        .frame(width: 200, height: 80, alignment: .center)
                        .background(Color.white)
                        .cornerRadius(25.0)
                        .opacity(0.6)
                             ,alignment:.centerLastTextBaseline
                    )
                
                ,
                alignment: .top
            )
        
            .overlay(
                Image(systemName: "ipad")
                    .imageScale(.large)
                    .font(.system(size:250))
                    .foregroundColor(.blue)
                
                    .overlay(
                        Image("aka")
                            .resizable()
                            .aspectRatio(contentMode:.fit)
                            .frame(width: 210, height: 210, alignment: .topLeading)
                        
                            .overlay(
                             Text("你不理財 財不理你")
                            .fontWeight(.heavy)
                            .lineSpacing(20)
                            .font(.system(size: 20))
                            .foregroundColor(.black)
                            .frame(width:180, height:30, alignment: .center)
                            .background(Color.white)
                            .cornerRadius(25.0)
                            .opacity(0.6)
                            ,alignment: .centerLastTextBaseline)
                    )
                
                ,alignment: .bottom
                
            )
    
    }
        
}

```
</td>
</tr>
</table>





