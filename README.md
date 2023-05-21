import java.util.Scanner;

public class Matrix {
    public static void main(String[] args){
        Scanner mat = new Scanner(System.in);

        System.out.print("Masukan Ordo Matriks(Baris x Kolom): ");
        int baris = mat.nextInt();
        int kolom = mat.nextInt();

        int [][] matrixx = new int[baris][kolom];
        int [][] matrikss = new int[baris][kolom];

        System.out.println();
        System.out.println("Bilangan/Elemen Pada Matriks A: ");
        bilMat(matrixx, mat);

        System.out.println();
        System.out.println("Bilangan/Elemen Pada Matriks B: ");
        bilMat(matrikss, mat);

        int [][] Jumlah = jumlahMat(matrixx,matrikss);

        System.out.println();
        System.out.println("Hasil dari Penjumlahan Matriks: ");
        hasilMatrix(Jumlah);

    }

    public static void bilMat(int [][] matrik, Scanner mat){
        int baris = matrik.length;
        int kolom = matrik[0].length;

        for (int i=0; i<baris; i++){
            for(int x=0; x<kolom; x++){
                System.out.print("Masukan Bilangan Pada Matriks [" +i+ "][" +x+ "]: ");
                matrik[i][x] = mat.nextInt();
            }
        }
    }

    public static int[][] jumlahMat(int[][] matrixx, int[][] matrikss){
        int baris = matrixx.length;
        int kolom = matrixx[0].length;

        int [][] Jumlah = new int[baris][kolom];

        for (int i=0;i<baris;i++){
            for (int x=0;x<kolom;x++){
                Jumlah[i][x] = matrixx[i][x] + matrikss[i][x];
            }
        }
        return Jumlah;
    }

    public static void hasilMatrix(int [][] matriks){
        int baris = matriks.length;
        int kolom = matriks[0].length;

        for (int i=0;i<baris;i++){
            for (int x=0;x<kolom;x++){
                System.out.print(matriks[i][x] + " ");
            }
            System.out.println();
        }
    }
}
