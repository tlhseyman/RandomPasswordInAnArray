package sample;

public class ArrayRandomPassword {
    public static void main(String[] args) {

    }
    public static String generateRandomPassword(){
        String password = null;
        String[][] myValues = {
                {"A","B","C","D","E","F","G","H","I","J","K","L","M","N","O","P","R","S","T","U","V","Y","Z"},
                {"a","b","c","d","e","f","g","h","i","j","k","l","m","n","o","p","r","s","t","u","v","y","z"},
                {"!","@","#","$","%","^","&","*","(",")","_","/","?","{","}","|","~",":",";",",",">","<","+"},
                {"1","2","3","4","5","6","7","8","9"}
        };
        double rand = Math.random();
        for (int i=0; i<4; i++){
            rand = Math.random()*23;
            password = password + myValues[0][(int) rand];
        }
        for(int j=0; j<4; j++){
            rand = Math.random()*23;
            password=password + myValues[1][(int) rand];

        }
        rand = Math.random()*23;
        password = password + myValues[2][(int) rand];

        return password;

    }
}
