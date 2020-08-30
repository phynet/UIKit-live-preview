
import Foundation
import SwiftUI

class CollectionController: UICollectionViewController {
    private let cellIdentifier = "cellId"

    init() {
        let layout = UICollectionViewFlowLayout()
        super.init(collectionViewLayout: layout)
    }

    override func viewDidLoad() {
        collectionView.backgroundColor = .white
        collectionView.register(UICollectionViewCell.self, forCellWithReuseIdentifier: cellIdentifier)
    }
    required init?(coder: NSCoder) {
        fatalError("init(coder:) has not been implemented")
    }
    
    override func collectionView(_ collectionView: UICollectionView, numberOfItemsInSection section: Int) -> Int {
        return 5
    }

    override func collectionView(_ collectionView: UICollectionView, cellForItemAt indexPath: IndexPath) -> UICollectionViewCell {
        let collectionCell = collectionView.dequeueReusableCell(withReuseIdentifier: cellIdentifier, for: indexPath)
        collectionCell.backgroundColor = [UIColor.green, .purple, .blue, .brown, .yellow].randomElement()
        return collectionCell
    }

}

struct ContentView_Previews: PreviewProvider {
    static var previews: some View {
        Container().edgesIgnoringSafeArea(.all)
    }

    struct Container: UIViewControllerRepresentable {
        func makeUIViewController(context: Context) -> UIViewController {
            UINavigationController(rootViewController: CollectionController())
        }

        func updateUIViewController(_ uiViewController: UIViewController, context: Context) {

        }

        typealias UIViewControllerType = UIViewController
    }
}

struct ContentView: View {
    var body: some View {
        Text("Hello")
    }
}
