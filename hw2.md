<h1>hw2</h1>
<table>
    <tr>
        <td>
            <img src="https://raw.githubusercontent.com/phhsu0508/swiftUI/main/hw2demo.mp4">
                </td>        
 <td>

  
```swift
import SwiftUI

struct ContentView: View 
{
    @State var count:Int = 0
    @State var me:Int = 0
    
        
        var content = ["剪刀", "石頭", "布"]
        var body: some View 
    {
        ZStack{
            Image("bg")
                .resizable()
                .scaledToFill()
                .opacity(0.3)
            VStack{
                if(count == me)
                {
                    HStack{
                        Text("Takina出"+content[count])
                            .padding(.all,5) 
                            .frame(alignment: .top) 
                            .font(.system(size: 30))
                            .background(Color.gray)
                            .foregroundColor(.white)
                        Text("平手")
                            .padding(.all,5) 
                            .frame(alignment: .center) 
                            .font(.system(size: 50))
                            .background(Color.gray)
                            .foregroundColor(.white)
                    }

                    Image("tie")
                        .resizable()
                        .scaledToFit()
                        .frame(width: 370, height: 250,
                               alignment: .center)
                    
                }
                
                if(me == 0)
                {
                    if(count == 1)
                    {
                        HStack{
                            Text("Takina出"+content[count])
                                .padding(.all,5) 
                                .frame(alignment: .top) 
                                .font(.system(size: 30))
                                .background(Color.gray)
                                .foregroundColor(.white)
                            Text("你輸了")
                                .padding(.all,5) 
                                .frame(alignment: .center) 
                                .font(.system(size: 40))
                                .background(Color.gray)
                            .foregroundColor(.white) }
                            Image("lose")
                                .resizable()
                                .frame(width: 370, height: 250,
                                       alignment: .center) 
                        
                            
                    }
                    else if(count == 2)
                    {
                        HStack{
                            Text("Takina出"+content[count])
                                .padding(.all,5) 
                                .frame(alignment: .top) 
                                .font(.system(size: 30))
                                .background(Color.gray)
                                .foregroundColor(.white)
                            Text("你贏了")
                                .padding(.all,5) 
                                .frame(alignment: .center) 
                                .font(.system(size: 50))
                                .background(Color.gray)
                                .foregroundColor(.white)
                        }
                        Image("win")
                            .resizable()
                            .frame(width: 370, height: 250,
                                   alignment: .center) 
                            
                    }
                }
                
                if(me == 1)
                {
                    if(count == 0)
                    {
                        HStack{
                        Text("Takina出"+content[count])
                            .padding(.all,5) 
                            .frame(alignment: .top) 
                            .font(.system(size: 30))
                            .background(Color.gray)
                            .foregroundColor(.white)
                        Text("你贏了")
                            .padding(.all,5) 
                            .frame(alignment: .center) 
                            .font(.system(size: 50))
                            .background(Color.gray)
                            .foregroundColor(.white)
                    }
                        Image("win")
                            .resizable()
                            .frame(width: 370, height: 250,
                                   alignment: .center) 
                    }
                    else if(count == 2)
                    {
                        HStack{
                            Text("Takina出"+content[count])
                                .padding(.all,5) 
                                .frame(alignment: .top) 
                                .font(.system(size: 30))
                                .background(Color.gray)
                                .foregroundColor(.white)
                            Text("你輸了")
                                .padding(.all,5) 
                                .frame(alignment: .center) 
                                .font(.system(size: 50))
                                .background(Color.gray)
                                .foregroundColor(.white)
                        }
                        Image("lose")
                            .resizable()
                            .frame(width: 370, height: 250,
                                   alignment: .center) 
                    }
                }
                
                if(me == 2)
                {
                    if(count == 1)
                    {
                        HStack{
                            Text("Takina出"+content[count])
                                .padding(.all,5) 
                                .frame(alignment: .top) 
                                .font(.system(size: 30))
                                .background(Color.gray)
                                .foregroundColor(.white)
                            Text("你贏了")
                                .padding(.all,5) 
                                .frame(alignment: .center) 
                                .font(.system(size: 50))
                                .background(Color.gray)
                                .foregroundColor(.white)
                        }
                        Image("win")
                            .resizable()
                            .frame(width: 370, height: 250,
                                   alignment: .center) 
                    }
                    else if(count == 0)
                    {
                        HStack{
                            Text("Takina出"+content[count])
                                .padding(.all,5) 
                                .frame(alignment: .top) 
                                .font(.system(size: 30))
                                .background(Color.gray)
                                .foregroundColor(.white)
                            Text("你輸了")
                                .padding(.all,5) 
                                .frame(alignment: .center) 
                                .font(.system(size: 50))
                                .background(Color.gray)
                                .foregroundColor(.white)
                        }
                        Image("lose")
                            .resizable()
                            .frame(width: 370, height: 250,
                                   alignment: .center) 
                    }
                }
                
                
                HStack{     
                    Button (action:
                                {
                        count = Int.random(in: 0..<3)
                        me = 0
                    }
                            , label: 
                                { Text("剪刀")
                            .padding(.all,5) 
                            .frame(alignment: .center) 
                            .font(.system(size: 50))
                            .background(Color.red)
                            .foregroundColor(.white) 
                            .border(Color.red, width: 5) 
                            .cornerRadius(20)
                    })
                    
                    Button (action:
                                {
                        count = Int.random(in: 0..<3)
                        me = 1
                    }
                            , label: 
                                { Text("石頭")
                            .padding(.all,5) 
                            .frame(alignment: .center) 
                            .font(.system(size: 50))
                            .background(Color.red)
                            .foregroundColor(.white) 
                            .border(Color.red, width: 5) 
                            .cornerRadius(20)
                    })
                    Button (action:
                                {
                        count = Int.random(in: 0..<3)
                        me = 2
                    }
                            , label: 
                                { Text("布")
                            .padding(.all,5) 
                            .frame(width:110,alignment: .center) 
                            .font(.system(size: 50))
                            .background(Color.red)
                            .foregroundColor(.white) 
                            .border(Color.red, width: 5) 
                            .cornerRadius(20)
                    })}
                
                
                
                
                
            }}}
    }
```
</td>
</tr>
</table>
