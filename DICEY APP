
import UIKit

class ViewController: UIViewController {
    //use hold ctrl and link images to code
    @IBOutlet weak var diceImageView1: UIImageView!
    
    @IBOutlet weak var diceImageView2: UIImageView!
    
    @IBOutlet weak var congratulations : UIImageView!
    
    var leftDiceNumber = 1
    var rightDiceNumber = 5
    
    @IBAction func rollButtonPressed(_ sender:UIButton) {
        
        let congoarray = [ #imageLiteral(resourceName: "congrats 1"), #imageLiteral(resourceName: "congrats 1"),  #imageLiteral(resourceName: "congrats 1"), #imageLiteral(resourceName: "congrats 1")]
        let diceArray=[ #imageLiteral(resourceName: "DiceOne"), #imageLiteral(resourceName: "DiceTwo"), #imageLiteral(resourceName: "DiceThree"), #imageLiteral(resourceName: "DiceFour"), #imageLiteral(resourceName: "DiceFive"), #imageLiteral(resourceName: "DiceSix")]
        congratulations.image = congoarray.randomElement()
        //var leftDiceNumber = 1
        //leftDiceNumber = 1
        print(leftDiceNumber);
        diceImageView1.image = diceArray.randomElement()
        diceImageView2.image = diceArray.randomElement()
          //if diceImageView1 == diceImageView2
            if leftDiceNumber == rightDiceNumber {
                congratulations.image = #imageLiteral(resourceName: "congrats 1")
                congratulations.isHidden = false
            } else {
                congratulations.isHidden = true
                
       
        
                
    
        // can also write the statement above as - [ #imageLiteral(resourceName: "DiceOne"), #imageLiteral(resourceName: "DiceTwo"), #imageLiteral(resourceName: "DiceThree"), #imageLiteral(resourceName: "DiceFour"), #imageLiteral(resourceName: "DiceFive"), #imageLiteral(resourceName: "DiceSix")][Int.random(in: 1...5)]
      }
    
}


        }
