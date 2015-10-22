# binSearch
二分探索の時間計算量
//---二分探索---//
static int binSearch(int[] a, int n, int key){
	int pl = 0;			//探索範囲先頭のインデックス
	int pr = n - 1;			//　　〃　末尾のインデックス　　
	
	do {
		int pc = (pl + pr)/2;	//中央要素のインデックス
		if (a[pc] == key)
			return pc;	//探索成功
		else if (a[pc] < key)
			pl = pc + 1;	//探索範囲を後半に絞り込む
		else
			pr = pc - 1;	//探索範囲を前半に絞り込む
	} while (pl <= pr);
	
	return -1;			//探索失敗
}
