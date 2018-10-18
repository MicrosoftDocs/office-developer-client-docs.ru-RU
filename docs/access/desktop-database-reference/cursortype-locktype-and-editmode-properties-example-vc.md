---
<span data-ttu-id="063c2-101"><<<<<<< Название HEAD: CursorType, LockType для и пример: свойства EditMode (VC ++) TOCTitle: CursorType, LockType для и пример: свойства EditMode (VC ++) === название: пример: свойства CursorType, LockType для и EditMode (VC ++) TOCTitle: Пример свойств CursorType, LockType для и EditMode (VC ++)</span><span class="sxs-lookup"><span data-stu-id="063c2-101"><<<<<<< HEAD title: CursorType, LockType, and EditMode Properties Example (VC++) TOCTitle: CursorType, LockType, and EditMode Properties Example (VC++) ======= title: CursorType, LockType, and EditMode properties example (VC++) TOCTitle: CursorType, LockType, and EditMode properties example (VC++)</span></span>
>>>>>>> <span data-ttu-id="063c2-102">главные ms:assetid: edbc4625-5013-cfcd-d709-ac8a85fe17b4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250205(v=office.15) ms:contentKeyID: 48548545 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="063c2-102">master ms:assetid: edbc4625-5013-cfcd-d709-ac8a85fe17b4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250205(v=office.15) ms:contentKeyID: 48548545 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="063c2-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="063c2-103"><<<<<<< HEAD</span></span>
# <a name="cursortype-locktype-and-editmode-properties-example-vc"></a><span data-ttu-id="063c2-104">CursorType, LockType, and EditMode Properties Example (VC++)</span><span class="sxs-lookup"><span data-stu-id="063c2-104">CursorType, LockType, and EditMode Properties Example (VC++)</span></span>
=======
# <a name="cursortype-locktype-and-editmode-properties-example-vc"></a><span data-ttu-id="063c2-105">Пример: свойства CursorType, LockType для и EditMode (VC ++)</span><span class="sxs-lookup"><span data-stu-id="063c2-105">CursorType, LockType, and EditMode properties example (VC++)</span></span>
>>>>>>> <span data-ttu-id="063c2-106">master</span><span class="sxs-lookup"><span data-stu-id="063c2-106">master</span></span>


<span data-ttu-id="063c2-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="063c2-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="063c2-108">В этом примере демонстрируется настройка свойств [CursorType](cursortype-property-ado.md) и [LockType для](locktype-property-ado.md) перед открытием [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="063c2-108">This example demonstrates setting the [CursorType](cursortype-property-ado.md) and [LockType](locktype-property-ado.md) properties before opening a [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="063c2-109">Также показано значение свойства [EditMode](editmode-property-ado.md) в различных условиях.</span><span class="sxs-lookup"><span data-stu-id="063c2-109">It also shows the value of the [EditMode](editmode-property-ado.md) property under various conditions.</span></span> <span data-ttu-id="063c2-110">Функция EditModeOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="063c2-110">The EditModeOutput function is required for this procedure to run.</span></span>

```cpp 
 
// BeginEditModeCpp 
#import "C:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <ole2.h> 
#include <stdio.h> 
#include <conio.h> 
 
// Function declaration 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void EditModeX(void); 
void EditModeOutput(char *, int); 
void PrintProviderError(_ConnectionPtr pConnection); 
void PrintComError(_com_error &e); 
 
/////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
/////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 EditModeX(); 
 
 // Wait here for the user to see the output 
 printf("\n\nPress any key to continue..."); 
 getch(); 
 
 ::CoUninitialize(); 
} 
 
/////////////////////////////////////////////////////////// 
// // 
// EditModeX Function // 
// // 
/////////////////////////////////////////////////////////// 
void EditModeX(void) 
{ 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace. 
 _RecordsetPtr pRstEmployees = NULL; 
 _ConnectionPtr pConnection = NULL; 
 
 HRESULT hr = S_OK; 
 
 _bstr_t strCnn("Provider='sqloledb';Data Source='MySqlServer';" 
 "Initial Catalog='pubs';Integrated Security='SSPI';"); 
 
 try 
 { 
 // Open a connection 
 TESTHR(pConnection.CreateInstance(__uuidof(Connection))); 
 hr = pConnection->Open(strCnn,"","",adConnectUnspecified); 
 
 // Open recordset with data from employee table 
 TESTHR(pRstEmployees.CreateInstance(__uuidof(Recordset))); 
 
 pRstEmployees->CursorLocation = adUseClient; 
 pRstEmployees->CursorType = adOpenStatic; 
 pRstEmployees->LockType = adLockBatchOptimistic; 
 
 pRstEmployees->Open("employee", 
 _variant_t((IDispatch *) pConnection,true), 
 adOpenStatic,adLockBatchOptimistic,adCmdTable); 
 
 // Show the EditMode property under different editing states. 
 pRstEmployees->AddNew (); 
 pRstEmployees->Fields->Item["emp_id"]->Value = 
 (_bstr_t)("T-T55555M"); 
 pRstEmployees->Fields->Item["fname"]->Value = 
 (_bstr_t)("temp_fname"); 
 pRstEmployees->Fields->Item["lname"]->Value = 
 (_bstr_t)("temp_lname"); 
 EditModeOutput("After AddNew: ", pRstEmployees->EditMode); 
 
 pRstEmployees->UpdateBatch(adAffectCurrent); 
 EditModeOutput("After Update: ", pRstEmployees->EditMode); 
 
 pRstEmployees->Fields->Item["fname"]->Value = (_bstr_t)("test"); 
 EditModeOutput("After Edit: ", pRstEmployees->EditMode); 
 
 // Delete new record because this is a demonstration. 
 pConnection->Execute("DELETE FROM employee WHERE emp_id = " 
 "'T-T55555M'", NULL, adCmdText); 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 // Pass a connection pointer accessed from the Recordset. 
 PrintProviderError(pConnection); 
 PrintComError(e); 
 } 
 
 // Clean up objects before exit. 
 if (pRstEmployees) 
 if (pRstEmployees->State == adStateOpen) 
 pRstEmployees->Close(); 
 if (pConnection) 
 if (pConnection->State == adStateOpen) 
 pConnection->Close(); 
} 
 
/////////////////////////////////////////////////////////// 
// // 
// EditModeOutput() Function // 
// // 
/////////////////////////////////////////////////////////// 
void EditModeOutput(char *strTemp, int intEditMode) 
{ 
 // Print report based on the value of the EditMode property. 
 printf("\n%s", strTemp); 
 printf("\n EditMode = "); 
 
 switch (intEditMode) 
 { 
 case adEditNone : 
 printf("adEditNone"); 
 break; 
 case adEditInProgress : 
 printf("adEditInProgress"); 
 break; 
 case adEditAdd : 
 printf("adEditAdd"); 
 break; 
 } 
} 
 
/////////////////////////////////////////////////////////// 
// // 
// PrintProviderError Function // 
// // 
/////////////////////////////////////////////////////////// 
 
void PrintProviderError(_ConnectionPtr pConnection) 
{ 
 // Print Provider Errors from Connection object. 
 // pErr is a record object in the Connection's Error collection. 
 ErrorPtr pErr = NULL; 
 
 if( (pConnection->Errors->Count) > 0) 
 { 
 long nCount = pConnection->Errors->Count; 
 // Collection ranges from 0 to nCount -1. 
 for(long i = 0; i < nCount; i++) 
 { 
 pErr = pConnection->Errors->GetItem(i); 
 printf("\n\t Error number: %x\t%s\n", pErr->Number, 
 (LPCSTR)pErr->Description); 
 } 
 } 
} 
 
/////////////////////////////////////////////////////////// 
// // 
// PrintComError Function // 
// // 
/////////////////////////////////////////////////////////// 
 
void PrintComError(_com_error &e) 
{ 
 _bstr_t bstrSource(e.Source()); 
 _bstr_t bstrDescription(e.Description()); 
 
 // Print Com errors. 
 printf("Error\n"); 
 printf("\tCode = %08lx\n", e.Error()); 
 printf("\tCode meaning = %s\n", e.ErrorMessage()); 
 printf("\tSource = %s\n", (LPCSTR) bstrSource); 
 printf("\tDescription = %s\n", (LPCSTR) bstrDescription); 
} 
 
// EndEditModeCpp 
```

