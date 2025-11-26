# DeepSeek_Unofficial
DeepSeek [ Version R2 ] ... Customized for Steam Game Platform ... No affiliated with DeepSeek ( based on Claude )

Probabaly not

#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <ctype.h>

// 構造体の定義 - 学生情報
struct Student {
    char name[50];      // 学生の名前
    int age;           // 年齢
    float gpa;         // GPA
};

// 列挙型 - 科目タイプ
enum SubjectType {
    MATH,              // 数学
    SCIENCE,           // 科学
    LITERATURE,        // 文学
    HISTORY,           // 歴史
    ART                // 美術
};

// 関数プロトタイプ宣言
void demonstrateDataTypeKeywords(void);
void demonstrateControlFlowKeywords(void);
void demonstrateStorageClassKeywords(void);
void demonstrateStructUnionEnum(void);
void demonstratePointerKeywords(void);
void demonstrateLoopKeywords(void);
void demonstrateJumpKeywords(void);
void demonstrateTypeQualifiers(void);
void demonstrateComplexKeywords(void);

// グローバル変数 - static記憶クラス
static int globalCounter = 0;

int main() {
    printf("=== C言語キーワード 9ケース デモンストレーション ===\n\n");
    
    // 9つのケースを順番に実行
    for(int i = 1; i <= 9; i++) {
        printf("\n🔰 ケース %d:\n", i);
        printf("═══════════════════════════════════\n");
        
        switch(i) {
            case 1:
                demonstrateDataTypeKeywords();     // データ型キーワード
                break;
            case 2:
                demonstrateControlFlowKeywords();  // 制御フローキーワード
                break;
            case 3:
                demonstrateStorageClassKeywords(); // 記憶クラスキーワード
                break;
            case 4:
                demonstrateStructUnionEnum();      // 構造体・共用体・列挙型
                break;
            case 5:
                demonstratePointerKeywords();      // ポインタ関連キーワード
                break;
            case 6:
                demonstrateLoopKeywords();         // ループ制御キーワード
                break;
            case 7:
                demonstrateJumpKeywords();         // ジャンプキーワード
                break;
            case 8:
                demonstrateTypeQualifiers();       // 型修飾子
                break;
            case 9:
                demonstrateComplexKeywords();      // 複合キーワード
                break;
            default:
                printf("未知のケースです\n");      // 未知のケース
                break;
        }
        
        printf("───────────────────────────────────\n");
    }
    
    printf("\n🎉 全てのケースの実行が完了しました！\n");
    return 0;
}

// ケース1: データ型キーワードのデモンストレーション
void demonstrateDataTypeKeywords(void) {
    printf("📊 データ型キーワード:\n");
    printf("   char, int, float, double, void\n\n");
    
    // 基本的なデータ型の宣言と使用
    char character = 'A';                    // char型 - 文字
    int integer = 42;                       // int型 - 整数
    float floatingPoint = 3.14f;            // float型 - 単精度浮動小数点数
    double doublePrecision = 2.71828;       // double型 - 倍精度浮動小数点数
    void *genericPointer = NULL;            // void型 - 汎用ポインタ
    
    printf("   char: '%c' (ASCII: %d)\n", character, character);
    printf("   int: %d\n", integer);
    printf("   float: %.2f\n", floatingPoint);
    printf("   double: %.5lf\n", doublePrecision);
    printf("   void*: %p (NULLポインタ)\n", genericPointer);
    
    // サイズの表示
    printf("\n   データ型のサイズ:\n");
    printf("   char: %zu bytes\n", sizeof(char));
    printf("   int: %zu bytes\n", sizeof(int));
    printf("   float: %zu bytes\n", sizeof(float));
    printf("   double: %zu bytes\n", sizeof(double));
    printf("   void*: %zu bytes\n", sizeof(void*));
}

// ケース2: 制御フローキーワードのデモンストレーション
void demonstrateControlFlowKeywords(void) {
    printf("🎛️  制御フローキーワード:\n");
    printf("   if, else, switch, case, default\n\n");
    
    int score = 85;
    
    // if-else 文のデモンストレーション
    printf("   if-else 文:\n");
    if(score >= 90) {
        printf("     評価: 優 (A)\n");           // 90点以上
    } else if(score >= 80) {
        printf("     評価: 良 (B)\n");           // 80-89点
    } else if(score >= 70) {
        printf("     評価: 可 (C)\n");           // 70-79点
    } else {
        printf("     評価: 不可 (F)\n");         // 70点未満
    }
    
    // switch-case 文のデモンストレーション
    printf("\n   switch-case 文:\n");
    int dayOfWeek = 3;
    
    switch(dayOfWeek) {
        case 1:
            printf("     月曜日\n");             // Monday
            break;
        case 2:
            printf("     火曜日\n");             // Tuesday
            break;
        case 3:
            printf("     水曜日\n");             // Wednesday
            break;
        case 4:
            printf("     木曜日\n");             // Thursday
            break;
        case 5:
            printf("     金曜日\n");             // Friday
            break;
        case 6:
            printf("     土曜日\n");             // Saturday
            break;
        case 7:
            printf("     日曜日\n");             // Sunday
            break;
        default:
            printf("     無効な日\n");           // Invalid day
            break;
    }
}

// ケース3: 記憶クラスキーワードのデモンストレーション
void demonstrateStorageClassKeywords(void) {
    printf("💾 記憶クラスキーワード:\n");
    printf("   auto, register, static, extern\n\n");
    
    // auto記憶クラス (ローカル変数)
    auto int localVar = 10;                 // auto - 自動記憶期間
    printf("   auto変数: %d\n", localVar);
    
    // register記憶クラス (レジスタ変数)
    register int counter;                   // register - レジスタ記憶クラス
    for(counter = 0; counter < 3; counter++) {
        printf("   register変数: %d\n", counter);
    }
    
    // static記憶クラス
    static int staticCounter = 0;           // static - 静的記憶期間
    staticCounter++;
    printf("   static変数: %d回目の呼び出し\n", staticCounter);
    
    // extern記憶クラス
    extern int globalCounter;               // extern - 外部リンケージ
    globalCounter++;
    printf("   extern変数 (globalCounter): %d\n", globalCounter);
}

// ケース4: 構造体・共用体・列挙型のデモンストレーション
void demonstrateStructUnionEnum(void) {
    printf("🏗️  構造体・共用体・列挙型:\n");
    printf("   struct, union, enum\n\n");
    
    // 構造体の使用
    struct Student student1;                // struct - 構造体
    strcpy(student1.name, "山田太郎");      // 名前の代入
    student1.age = 20;                      // 年齢の代入
    student1.gpa = 3.75f;                   // GPAの代入
    
    printf("   構造体 - 学生情報:\n");
    printf("     名前: %s\n", student1.name);
    printf("     年齢: %d歳\n", student1.age);
    printf("     GPA: %.2f\n", student1.gpa);
    
    // 共用体のデモンストレーション
    union Data {                            // union - 共用体
        int i;
        float f;
        char str[20];
    } data;
    
    data.i = 100;
    printf("\n   共用体 - 整数値: %d\n", data.i);
    data.f = 220.5;
    printf("   共用体 - 浮動小数点数: %.1f\n", data.f);
    strcpy(data.str, "こんにちは");
    printf("   共用体 - 文字列: %s\n", data.str);
    
    // 列挙型のデモンストレーション
    enum SubjectType subject = SCIENCE;     // enum - 列挙型
    printf("\n   列挙型 - 科目タイプ: ");
    
    switch(subject) {
        case MATH:
            printf("数学\n");               // Mathematics
            break;
        case SCIENCE:
            printf("科学\n");               // Science
            break;
        case LITERATURE:
            printf("文学\n");               // Literature
            break;
        case HISTORY:
            printf("歴史\n");               // History
            break;
        case ART:
            printf("美術\n");               // Art
            break;
    }
}

// ケース5: ポインタ関連キーワードのデモンストレーション
void demonstratePointerKeywords(void) {
    printf("📍 ポインタ関連キーワード:\n");
    printf("   *, &, sizeof\n\n");
    
    int number = 100;
    int *pointer = &number;                 // * - ポインタ宣言, & - アドレス演算子
    
    printf("   変数 'number':\n");
    printf("     値: %d\n", number);
    printf("     アドレス: %p\n", &number);
    printf("     サイズ: %zu bytes\n", sizeof(number));
    
    printf("\n   ポインタ 'pointer':\n");
    printf("     ポインタの値 (アドレス): %p\n", pointer);
    printf("     間接参照値: %d\n", *pointer);  // * - 間接参照演算子
    printf("     ポインタ自体のアドレス: %p\n", &pointer);
    printf("     ポインタのサイズ: %zu bytes\n", sizeof(pointer));
    
    // 配列とポインタ演算
    int array[5] = {10, 20, 30, 40, 50};
    int *arrPtr = array;
    
    printf("\n   配列とポインタ演算:\n");
    printf("     配列の先頭アドレス: %p\n", array);
    printf("     ポインタ演算 *(arrPtr + 2): %d\n", *(arrPtr + 2));
}

// ケース6: ループ制御キーワードのデモンストレーション
void demonstrateLoopKeywords(void) {
    printf("🔄 ループ制御キーワード:\n");
    printf("   for, while, do-while, break, continue\n\n");
    
    // forループ
    printf("   forループ:\n");
    for(int i = 1; i <= 5; i++) {          // for - ループ制御
        if(i == 3) continue;               // continue - 次の繰り返しへ
        printf("     i = %d\n", i);
    }
    
    // whileループ
    printf("\n   whileループ:\n");
    int count = 5;
    while(count > 0) {                     // while - ループ制御
        printf("     カウント: %d\n", count);
        if(count == 2) break;              // break - ループ脱出
        count--;
    }
    
    // do-whileループ
    printf("\n   do-whileループ:\n");
    int value = 3;
    do {                                   // do-while - ループ制御
        printf("     値: %d\n", value);
        value--;
    } while(value > 0);
}

// ケース7: ジャンプキーワードのデモンストレーション
void demonstrateJumpKeywords(void) {
    printf("🏃 ジャンプキーワード:\n");
    printf("   goto, return\n\n");
    
    printf("   return文のデモンストレーション:\n");
    
    // 関数内でのreturnの使用
    int result = calculateSum(5, 3);       // return - 値の返却
    printf("     計算結果: %d\n", result);
    
    // goto文のデモンストレーション
    printf("\n   goto文のデモンストレーション:\n");
    int i = 0;
    
start_label:                               // ラベルの定義
    if(i >= 3) {
        goto end_label;                    // goto - 条件付きジャンプ
    }
    printf("     繰り返し %d\n", i + 1);
    i++;
    goto start_label;                      // goto - 無条件ジャンプ
    
end_label:
    printf("   gotoループ終了\n");
}

// 補助関数 - 合計計算
int calculateSum(int a, int b) {
    return a + b;                          // return - 関数からの値返却
}

// ケース8: 型修飾子のデモンストレーション
void demonstrateTypeQualifiers(void) {
    printf("🛡️  型修飾子:\n");
    printf("   const, volatile, restrict\n\n");
    
    // const修飾子
    const int MAX_VALUE = 100;             // const - 定数修飾子
    printf("   const定数: MAX_VALUE = %d\n", MAX_VALUE);
    
    // constポインタ
    int value = 50;
    const int *ptr1 = &value;              // const - ポインタ経由の変更禁止
    int *const ptr2 = &value;              // const - ポインタ自体の変更禁止
    const int *const ptr3 = &value;        // const - 両方の変更禁止
    
    printf("   constポインタ:\n");
    printf("     const int*: ポインタ経由の変更禁止\n");
    printf("     int* const: ポインタ自体の変更禁止\n");
    printf("     const int* const: 両方の変更禁止\n");
    
    // volatile修飾子
    volatile int sensorValue = 0;          // volatile - 最適化抑制
    printf("\n   volatile変数: コンパイラの最適化を抑制\n");
    
    // restrict修飾子 (C99)
    int array1[5] = {1, 2, 3, 4, 5};
    int array2[5] = {6, 7, 8, 9, 10};
    
    copyArrays(array1, array2, 5);         // restrict - ポインタエイリアシングの制限
    printf("   restrict修飾子: ポインタエイリアシングの制限\n");
}

// restrict修飾子を使用した関数
void copyArrays(int *restrict dest, const int *restrict src, size_t n) {
    for(size_t i = 0; i < n; i++) {
        dest[i] = src[i];                  // restrict - 最適化のためのヒント
    }
}

// ケース9: 複合キーワードのデモンストレーション
void demonstrateComplexKeywords(void) {
    printf("🧩 複合キーワード:\n");
    printf("   typedef, sizeof, _Bool, _Complex, _Imaginary\n\n");
    
    // typedefの使用
    typedef unsigned int uint;             // typedef - 型の別名定義
    typedef struct {
        char brand[20];
        float price;
    } Car;
    
    uint distance = 500;                   // typedefで定義された型の使用
    Car myCar;
    strcpy(myCar.brand, "トヨタ");
    myCar.price = 2500000.0f;
    
    printf("   typedefの使用:\n");
    printf("     符号なし整数: %u\n", distance);
    printf("     車: %s - %.2f円\n", myCar.brand, myCar.price);
    
    // sizeof演算子
    printf("\n   sizeof演算子:\n");
    printf("     intのサイズ: %zu bytes\n", sizeof(int));
    printf("     doubleのサイズ: %zu bytes\n", sizeof(double));
    printf("     Car構造体のサイズ: %zu bytes\n", sizeof(Car));
    
    // _Bool型 (C99)
    _Bool isTrue = 1;                      // _Bool - 真偽値型
    _Bool isFalse = 0;
    
    printf("\n   _Bool型 (C99):\n");
    printf("     真: %d\n", isTrue);
    printf("     偽: %d\n", isFalse);
    
    // 複素数型 (C99)
    #ifdef __STDC_IEC_559_COMPLEX__
    double _Complex complexNum = 3.0 + 4.0 * I;  // _Complex - 複素数型
    printf("\n   複素数型 (C99):\n");
    printf("     複素数: %.1f + %.1fi\n", creal(complexNum), cimag(complexNum));
    #else
    printf("\n   複素数型: この環境ではサポートされていません\n");
    #endif
}
// グローバル変数の定義
int globalCounter = 0;
