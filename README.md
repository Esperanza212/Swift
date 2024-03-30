import SwiftUI

struct ContentView: View {
    @State private var labelText = "Hello, World!"
    
    var body: some View {
        VStack {
            Text(labelText)
                .padding()
            
            Button(action: {
                self.labelText = "Button tapped!"
            }) {
                Text("Tap me!")
                    .padding()
                    .background(Color.blue)
                    .foregroundColor(Color.white)
                    .cornerRadius(10)
            }
        }
    }
}

struct ContentView_Previews: PreviewProvider {
    static var previews: some View {
        ContentView()
    }
}
