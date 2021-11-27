# tourist-app
import UIKit

class ViewController: UIViewController {
    
    var placecount: Int = 0
    @IBOutlet weak var imgplace: UIImageView!
    @IBOutlet weak var lblplaces: UILabel!
    @IBOutlet weak var imgdetails: UILabel!
    let placeArray = ["thalassery fort","paithallmala","palakayamthattu","nedumpoil","kadalpalam"]
    let DetailsArray = ["Thalassery fort is one of the most beautiful peaks in the Western Ghats that mesmerizes anyone who has been here. Standing tall at 4500 ft, Paithalmala is the tallest peak in the district of Kannur and a very popular trekking destination for all the nature and adventure lovers out there.","paithallmala is one of the most beautiful peaks in the Western Ghats that mesmerizes anyone who has been here. Standing tall at 4500 ft, Paithalmala is the tallest peak in the district of Kannur and a very popular trekking destination for all the nature and adventure lovers","palakayamthattu is one of the most beautiful peaks in the Western Ghats that mesmerizes anyone who has been here. Standing tall at 4500 ft, Paithalmala is the tallest peak in the district of Kannur and a very popular trekking destination for all the nature and adventure lovers","nedumpoil is one of the most beautiful peaks in the Western Ghats that mesmerizes anyone who has been here. Standing tall at 4500 ft, Paithalmala is the tallest peak in the district of Kannur and a very popular trekking destination for all the nature and adventure lovers","kadalpalam is one of the most beautiful peaks in the Western Ghats that mesmerizes anyone who has been here. Standing tall at 4500 ft, Paithalmala is the tallest peak in the district of Kannur and a very popular trekking destination for all the nature and adventure lovers"]
    
    override func viewDidLoad() {
        super.viewDidLoad()
        imgplace.image = UIImage(named: placeArray[0])
        lblplaces.text = placeArray[0]
        imgdetails.text = DetailsArray[0]
    }
    @IBAction func nextbtn(_ sender: UIButton) {
        placecount = placecount + 1
        if placecount <= 4 {
            imgplace.image = UIImage(named : placeArray[placecount] )
            imgdetails.text = DetailsArray[placecount]
            lblplaces.text = placeArray[placecount]
        }else {
            placecount = -1
        }
    }
   
    @IBAction func backbtn(_ sender: UIButton) {
        placecount = placecount - 1
                      if placecount >= 0 {
                          imgplace.image = UIImage(named : placeArray[placecount] )
                          imgdetails.text = DetailsArray[placecount]
                          lblplaces.text = placeArray[placecount]
                      }else {
                          placecount = 5
                      }
           }
    }


