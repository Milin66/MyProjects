//
//  ContentView.swift
//  chatAI
//
//  Created by Milin Agarwal  on 07/07/23.
//
import OpenAISwift
import SwiftUI

final class Viewmodel: ObservableObject {
    init() {}
    private var client : OpenAISwift?
        func setup() {
            client = OpenAISwift(authToken: "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")
            
        }
    
    //i need to understand the section below better 
    func send(text:String,
              completion: @escaping(String) -> Void) {
        client?.sendCompletion(with: text,
                               maxTokens: 1000,
                               completionHandler: { result in
            switch result {
            case .success(let model):
                let output = model.choices?.first?.text ?? ""
                completion(output)
            case .failure(_):
                break
                
            }
        })
        
    }
    
    struct ContentView : View {
        @ObservedObject var viewmodel = Viewmodel()
        @State var text = ""
        @State var models = [String]()
        var body: some View {
            VStack(alignment: .leading) {
                ForEach(models, id: \.self) { string in
                    Text(string)
                }
                
                Spacer()
                
                HStack{
                    TextField("Type Here.....", text: $text)
                    Button("send") {
                        send()
                        
                    }
                }
            }
            .onAppear{
                viewmodel.setup()
            }
            .padding()
        }
      
        
        func send() {
            guard !text.trimmingCharacters(in: .whitespaces).isEmpty else {
                return
            }
            models.append("Me: \(text)")
            viewmodel.send(text: text) { response in
                DispatchQueue.main.async {
                    self.models.append("CHATGPT: "+response)
                    self.text=""
                }
                
            }
        }
        
        struct ContentView_Previews: PreviewProvider {
            static var previews: some View {
                ContentView()
            }
        }
        
    }
    
}

//convert contentview from local to global
// if we use "struct" before the variable it can already be used globally

