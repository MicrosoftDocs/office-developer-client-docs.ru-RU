---
title: Sort Property Example (VC++)
TOCTitle: Sort Property Example (VC++)
ms:assetid: 0f32b7ac-1902-1753-0c03-b38ba8c10c9c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248862(v=office.15)
ms:contentKeyID: 48543259
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 33f8134320192ad22b0ddc743c1e445cfad46d58
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482592"
---
# <a name="sort-property-example-vc"></a>Sort Property Example (VC++)


**Применимо к**: Access 2013 | Office 2013

В этом примере используется свойство [сортировки](sort-property-ado.md) объекта [набора записей](recordset-object-ado.md) для изменения порядка строк **набора записей** , полученных из таблицы ***авторов*** базы данных **Pubs** . Дополнительный служебной процедуры печатает каждую строку.

```cpp 
 
// BeginSortCpp 
#import "C:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <ole2.h> 
#include <stdio.h> 
#include <conio.h> 
 
// Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void SortX(void); 
void SortXprint(_bstr_t title, _RecordsetPtr rstp); 
void PrintProviderError(_ConnectionPtr pConnection); 
void PrintComError(_com_error &e); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 SortX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// SortX Function // 
// // 
////////////////////////////////////////////////////////// 
void SortX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace. 
 _ConnectionPtr pConnection = NULL; 
 _RecordsetPtr pRstAuthors = NULL; 
 
 // Define string variables. 
 _bstr_t strCnn("Provider='sqloledb';Data Source='MySqlServer';" 
 "Initial Catalog='pubs';Integrated Security='SSPI';"); 
 
 try 
 { 
 TESTHR(pConnection.CreateInstance(__uuidof(Connection))); 
 
 TESTHR(pRstAuthors.CreateInstance(__uuidof(Recordset))); 
 
 pRstAuthors->CursorLocation = adUseClient; 
 pConnection->Open (strCnn, "", "", adConnectUnspecified); 
 pRstAuthors->Open("SELECT * FROM authors", 
 _variant_t((IDispatch *) pConnection), 
 adOpenStatic, adLockReadOnly, adCmdText); 
 
 SortXprint(" Initial Order ", pRstAuthors); 
 
 //Clear the screen for the next display. 
 printf("\nPress any key to continue..."); 
 getch(); 
 system("cls"); 
 
 pRstAuthors->Sort = "au_lname ASC, au_fname ASC"; 
 SortXprint("Last Name Ascending", pRstAuthors); 
 
 //Clear the screen for the next display. 
 printf("\nPress any key to continue..."); 
 getch(); 
 system("cls"); 
 
 pRstAuthors->Sort = "au_lname DESC, au_fname ASC"; 
 SortXprint("Last Name Descending", pRstAuthors); 
 } 
 catch(_com_error &e) 
 { 
 PrintProviderError(pConnection); 
 PrintComError(e); 
 } 
 
 // Clean up objects before exit. 
 if (pRstAuthors) 
 if (pRstAuthors->State == adStateOpen) 
 pRstAuthors->Close(); 
 if (pConnection) 
 if (pConnection->State == adStateOpen) 
 pConnection->Close(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// SortXprint Function // 
// // 
////////////////////////////////////////////////////////// 
//This is the secondary utility routine that prints 
//the given title, and the contents of the specified Recordset. 
void SortXprint(_bstr_t title, _RecordsetPtr rstp) 
{ 
 printf("---------------%s---------------\n", (LPCSTR)title); 
 printf("First Name Last Name\n" 
 "---------------------------------------------------\n"); 
 rstp->MoveFirst(); 
 int intLineCnt = 4; 
 while (!(rstp->EndOfFile)) 
 { 
 _bstr_t aufname; 
 _bstr_t aulname; 
 aufname = rstp->GetFields()->GetItem("au_fname")->Value; 
 aulname = rstp->GetFields()->GetItem("au_lname")->Value, 
 printf("%s %s\n",(LPCSTR) aufname, (LPCSTR) aulname); 
 rstp->MoveNext(); 
 intLineCnt++; 
 if (intLineCnt % 20 ==0) 
 { 
 printf("\nPress any key to continue...\n"); 
 getch(); 
 } 
 } 
} 
 
////////////////////////////////////////////////////////// 
// // 
// PrintProviderError Function // 
// // 
////////////////////////////////////////////////////////// 
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
 printf("Error number: %x\t%s\n", pErr->Number, 
 (LPCSTR) pErr->Description); 
 } 
 } 
} 
 
////////////////////////////////////////////////////////// 
// // 
// PrintComError Function // 
// // 
////////////////////////////////////////////////////////// 
 
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
 
// EndSortCpp 
```
