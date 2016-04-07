import java.util.Scanner;

public class Special {
public static void main(String[] args) {
	Scanner sc = new Scanner(System.in);
	int testCase = sc.nextInt();
	int problemPerPage = sc.nextInt();
	int page =0;
	int special = 0;
	
	for(int i=0;i< testCase;i++){
		int prob = sc.nextInt();
		int all=0;
		
		while(prob>=problemPerPage){
			page++;
			if((page > all )&& (page<= all+problemPerPage)){
				special++;
				prob= prob-problemPerPage;
				all=all+problemPerPage;
				
			}else{
				prob= prob-problemPerPage;
				all=all+problemPerPage;
			}
		}
		if(prob>0){
		page++;
		while(prob>0 &&(prob<problemPerPage)){
			all++;
			if(page ==all){
				special++;
			}
			prob--;
		}
	}
		
	}
	System.out.println(special);
}
}
