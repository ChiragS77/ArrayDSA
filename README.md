# ArrayDSA
This module is about array dsa questions
![1_X0Dg7QfSYtWhSAu-afi8-g](https://github.com/ChiragS77/ArrayDSA/assets/142990449/443acbf6-5e50-492c-bc69-93a05d43396a)


//Find the peak Element in array

    public static int findPeakElement(int arr[]){
        int start = 0;
        int end = arr.length -1;

        while(start<end){
            int mid = start + (start -end)/2;

            if(arr[mid]< arr[mid+1]){
                start= mid +1;
            }
            else{
                end = mid;
            }
        }
        return end;
    }

    public static boolean isPeak(int arr[], int index){
        int length = arr.length;

        if(index <0 || index > length){
            return false;
        }

        if(index ==0 || arr[index] >= arr[index-1] && index==length-1 || arr[index] >= arr[index + 1]){
            return true;
        }
        return false;
    }

    public static void main(String[] args) {
        int[] arr = {1, 3, 20, 4, 1, 0};
        int peakIdx = findPeakElement(arr);

      boolean result =   isPeak(arr,peakIdx);
      System.out.println(result);

    }
}

}
