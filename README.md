# Factory_Design_pattern_java\
public class lab1{
public static void main(String ...args){
    FruitFActory ff=new FruitFActory();
    fruit name=ff.provideFruit("apple");
    name.produceJuice();
}
}
interface fruit{
    void produceJuice();
}
class Apple implements fruit{
      public void produceJuice()
      {
        System.out.println("your Apple juice is ready");
      }
}
class Banana implements fruit{
     public void produceJuice()
      {
        System.out.println("your Banana juice is ready");
      }

}
class Orange implements fruit{
     public void produceJuice()
      {
        System.out.println("your Orange juice is ready");
      }

}
class FruitFActory{
    fruit provideFruit(String s){
        switch(s){
            case "Apple":
                return new Apple();
            case "Banana":
                return new Banana();
            case "Orange":
                return new Orange();
            default:
                 return new Apple();


        }
    }
}
