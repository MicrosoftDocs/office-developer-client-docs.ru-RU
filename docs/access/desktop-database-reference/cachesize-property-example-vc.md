---
title: Пример использования свойства CacheSize (VC++)
TOCTitle: CacheSize property example (VC++)
ms:assetid: bd5bc7ae-c1fa-361b-9b26-a216655e3cbd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249914(v=office.15)
ms:contentKeyID: 48547435
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 819c6adee877de66299af4f1e234f1e2886b6bd2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296733"
---
# <a name="cachesize-property-example-vc"></a>Пример использования свойства CacheSize (VC++)


**Область применения**: Access 2013, Office 2013

В этом примере свойство [CacheSize](cachesize-property-ado.md) показывает разницу в производительности для операции, выполненной с кэшом с 30 записью и без него.

```cpp 
 
// BeginCacheSizeCpp 
#import "C:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <ole2.h> 
#include <stdio.h> 
#include <conio.h> 
#include <winbase.h> 
 
// Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void CacheSizeX(); 
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
 
 CacheSizeX(); 
 
 //Wait here for user to see the output.. 
 printf("\nPress any key to continue..."); 
 getch(); 
 
 ::CoUninitialize(); 
} 
 
/////////////////////////////////////////////////////////// 
// // 
// CacheSizeX Function // 
// // 
/////////////////////////////////////////////////////////// 
 
void CacheSizeX() 
{ 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace 
 _RecordsetPtr pRstRoySched = NULL; 
 
 //Define Other Variables 
 HRESULT hr = S_OK; 
 DWORD sngStart; 
 DWORD sngEnd; 
 float sngNoCache; 
 float sngCache; 
 int intLoop = 0; 
 _bstr_t strTemp; 
 
 _bstr_t strCnn("Provider='sqloledb';Data Source='MySqlServer';" 
 "Initial Catalog='pubs';Integrated Security='SSPI';"); 
 
 try 
 { 
 //Open the RoySched table. 
 TESTHR(pRstRoySched.CreateInstance(__uuidof(Recordset))); 
 pRstRoySched->Open("roysched", strCnn, adOpenForwardOnly, 
 adLockReadOnly, adCmdTable); 
 
 // Enumerate the Recordset object twice and record 
 // the elapsed time. 
 sngStart = GetTickCount(); 
 
 for (intLoop = 1; intLoop < 2; intLoop++) 
 { 
 pRstRoySched->MoveFirst(); 
 
 while(!(pRstRoySched->EndOfFile)) 
 { 
 // Execute a simple operation for the 
 // performance test. 
 strTemp = pRstRoySched->Fields-> 
 Item["title_id"]->Value; 
 pRstRoySched->MoveNext(); 
 } 
 } 
 sngEnd = GetTickCount(); 
 sngNoCache = (float)(sngEnd - sngStart)/(float)1000; 
 
 // Cache records in groups of 30 records. 
 pRstRoySched->MoveFirst(); 
 pRstRoySched->CacheSize = 30; 
 
 sngStart = GetTickCount(); 
 
 // Enumerate the Recordset object twice and record 
 // the elapsed time. 
 for (intLoop = 1;intLoop < 2; intLoop++) 
 { 
 pRstRoySched->MoveFirst(); 
 while(!(pRstRoySched->EndOfFile)) 
 { 
 // Execute a simple operation for the 
 // performance test. 
 strTemp = pRstRoySched->Fields-> 
 Item["title_id"]->Value; 
 pRstRoySched->MoveNext(); 
 } 
 } 
 sngEnd = GetTickCount(); 
 sngCache = (float)(sngEnd - sngStart)/(float)1000; 
 
 // Display performance results. 
 printf("Caching Performance Results:\n"); 
 printf("No cache: %6.3f seconds \n", sngNoCache); 
 printf("30-record cache: %6.3f seconds \n", sngCache); 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 _variant_t vtConnect = pRstRoySched->GetActiveConnection(); 
 
 // GetActiveConnection returns connect string if connection 
 // is not open, else returns Connection object. 
 switch(vtConnect.vt) 
 { 
 case VT_BSTR: 
 PrintComError(e); 
 break; 
 case VT_DISPATCH: 
 // Pass a connection pointer accessed from the Recordset. 
 PrintProviderError(vtConnect); 
 break; 
 default: 
 printf("Errors occured."); 
 break; 
 } 
 } 
 
 // Clean up objects before exit. 
 if (pRstRoySched) 
 if (pRstRoySched->State == adStateOpen) 
 pRstRoySched->Close(); 
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
 printf("Error number: %x\t%s", pErr->Number, 
 pErr->Description); 
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
// EndCacheSizeCpp 
```

