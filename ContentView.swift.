import SwiftUI  
  
struct ContentView: View {  
      
    @State private var tasks: [String] = []  
    @State private var newTask: String = ""  
      
    var body: some View {  
        VStack {  
              
            Text("My Tasks 📝")  
                .font(.largeTitle)  
                .padding()  
              
            HStack {  
                TextField("Enter new task", text: $newTask)  
                    .textFieldStyle(RoundedBorderTextFieldStyle())  
                  
                Button(action: {  
                    addTask()  
                }) {  
                    Text("Add")  
                        .padding(8)  
                        .background(Color.blue)  
                        .foregroundColor(.white)  
                        .cornerRadius(8)  
                }  
            }  
            .padding()  
              
            List {  
                ForEach(tasks, id: \.self) { task in  
                    Text(task)  
                }  
                .onDelete(perform: deleteTask)  
            }  
        }  
    }  
      
    func addTask() {  
        if !newTask.isEmpty {  
            tasks.append(newTask)  
            newTask = ""  
        }  
    }  
      
    func deleteTask(at offsets: IndexSet) {  
        tasks.remove(atOffsets: offsets)  
    }  
}  
  
#Preview {  
    ContentView()  
}  
