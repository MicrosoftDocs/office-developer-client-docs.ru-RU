---
title: Пример использования методов Save и Open (VC++)
TOCTitle: Save and Open methods example (VC++)
ms:assetid: 83e9647e-5dbd-2c59-4fff-2a3df79ab93c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249574(v=office.15)
ms:contentKeyID: 48546019
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54fb42ade164ce49cd09ce5a71b342342026a0a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308976"
---
# <a name="save-and-open-methods-example-vc"></a><span data-ttu-id="ce466-102">Пример использования методов Save и Open (VC++)</span><span class="sxs-lookup"><span data-stu-id="ce466-102">Save and Open methods example (VC++)</span></span>


<span data-ttu-id="ce466-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ce466-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ce466-104">В этих трех примерах  показано, как можно совместно использовать методы [Сохранить](save-method-ado.md) и Открыть.</span><span class="sxs-lookup"><span data-stu-id="ce466-104">These three examples demonstrate how the [Save](save-method-ado.md) and **Open** methods can be used together.</span></span>

<span data-ttu-id="ce466-105">Предположим, что вы собираетесь в командировку и хотите взять таблицу из базы данных.</span><span class="sxs-lookup"><span data-stu-id="ce466-105">Assume you are going on a business trip and want to take along a table from a database.</span></span> <span data-ttu-id="ce466-106">Перед входом вы можете получить доступ к данным в виде [наборов записей](recordset-object-ado.md) и сохранить их в транспортируемых формах.</span><span class="sxs-lookup"><span data-stu-id="ce466-106">Before you go, you access the data as a [Recordset](recordset-object-ado.md) and save it in a transportable form.</span></span> <span data-ttu-id="ce466-107">По прибытии в пункт назначения вы можете получить доступ к **Набору записей** в качестве локального отключенного **наборов записей.**</span><span class="sxs-lookup"><span data-stu-id="ce466-107">When you arrive at your destination, you access the **Recordset** as a local, disconnected **Recordset**.</span></span> <span data-ttu-id="ce466-108">Вы внося изменения в **Набор записей,** а затем сохраните его снова.</span><span class="sxs-lookup"><span data-stu-id="ce466-108">You make changes to the **Recordset**, then save it again.</span></span> <span data-ttu-id="ce466-109">Наконец, когда вы возвращаетесь домой, вы снова подключаетесь к базе данных и обновляете ее с помощью изменений, внесенных на дороге.</span><span class="sxs-lookup"><span data-stu-id="ce466-109">Finally, when you return home, you connect to the database again and update it with the changes you made on the road.</span></span>

```cpp 
 
// BeginSaveCpp 
#import "c:\Program Files\Common Files\system\ado\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <ole2.h> 
#include <stdio.h> 
#include <conio.h> 
#include <io.h> 
 
//Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
bool FileExists(void); 
void SaveX1(void); 
void SaveX2(void); 
void SaveX3(void); 
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
 
 //If File exists in the specified directory, then display error 
 if (!FileExists()) 
 { 
 SaveX1(); 
 SaveX2(); 
 SaveX3(); 
 } 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// SaveX1 Function // 
// // 
////////////////////////////////////////////////////////// 
 
//First, access and save the authors table. 
void SaveX1() 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace. 
 _RecordsetPtr pRstAuthors = NULL; 
 
 //Definitions of other variables 
 _bstr_t strCnn("Provider='sqloledb';Data Source='MySqlServer';" 
 "Initial Catalog='pubs';Integrated Security='SSPI';"); 
 
 try 
 { 
 TESTHR(pRstAuthors.CreateInstance(__uuidof(Recordset))); 
 
 pRstAuthors->Open("SELECT * FROM authors",strCnn, 
 adOpenDynamic,adLockBatchOptimistic,adCmdText); 
 
 // For sake of illustration, save the Recordset to a diskette 
 // in XML format. 
 pRstAuthors->Save("c:\\pubs.xml",adPersistXML); 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 // Pass a connection pointer accessed from the Recordset. 
 _variant_t vtConnect = pRstAuthors->GetActiveConnection(); 
 
 // GetActiveConnection returns connect string if connection 
 // is not open, else returns Connection object. 
 switch(vtConnect.vt) 
 { 
 case VT_BSTR: 
 PrintComError(e); 
 break; 
 case VT_DISPATCH: 
 PrintProviderError(vtConnect); 
 break; 
 default: 
 printf("Errors occured."); 
 break; 
 } 
 } 
 
 if (pRstAuthors) 
 if (pRstAuthors->State == adStateOpen) 
 pRstAuthors->Close(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// SaveX2 Function // 
// // 
////////////////////////////////////////////////////////// 
//At this point, you have arrived at your destination. 
//You will access the authors table as a local, disconnected Recordset. 
//Don't forget you must have the MSPersist provider on the machine you 
//are using in order to access the saved file, c:\pubs.xml. 
void SaveX2() 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace. 
 _RecordsetPtr pRstAuthors = NULL; 
 
 try 
 { 
 TESTHR(pRstAuthors.CreateInstance(__uuidof(Recordset))); 
 
 //For sake of illustration, we specify all parameters. 
 pRstAuthors->Open("c:\\pubs.xml","Provider='MSPersist';", 
 adOpenForwardOnly,adLockBatchOptimistic,adCmdFile); 
 
 //Now you have a local, disconnected Recordset. 
 //Edit it as you desire. 
 //(In this example, the change makes no difference). 
 pRstAuthors->Find("au_lname = 'Carson'",NULL,adSearchForward); 
 if (pRstAuthors->EndOfFile) 
 { 
 printf("Name not found ...\n"); 
 pRstAuthors->Close(); 
 return; 
 } 
 pRstAuthors->GetFields()->GetItem("City")->PutValue("Chicago"); 
 pRstAuthors->Update(); 
 
 // Save changes in ADTG format this time, purely for sake of 
 // illustration. Note that the previous version is still on the 
 // diskette as c:\pubs.xml. 
 pRstAuthors->Save("c:\\pubs.adtg",adPersistADTG); 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 // Pass a connection pointer accessed from the Recordset. 
 _variant_t vtConnect = pRstAuthors->GetActiveConnection(); 
 
 // GetActiveConnection returns connect string if connection 
 // is not open, else returns Connection object. 
 switch(vtConnect.vt) 
 { 
 case VT_BSTR: 
 PrintComError(e); 
 break; 
 case VT_DISPATCH: 
 PrintProviderError(vtConnect); 
 break; 
 default: 
 printf("Errors occured."); 
 break; 
 } 
 } 
 
 if (pRstAuthors) 
 if (pRstAuthors->State == adStateOpen) 
 pRstAuthors->Close(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// SaveX3 Function // 
// // 
////////////////////////////////////////////////////////// 
//Finally, you return home. Now update the database with 
//your changes. 
void SaveX3() 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace. 
 _RecordsetPtr pRstAuthors = NULL; 
 _ConnectionPtr pCnn = NULL; 
 
 //Definitions of other variables 
 _bstr_t strCnn("Provider='sqloledb';Data Source='MySqlServer';" 
 "Initial Catalog='pubs';Integrated Security='SSPI';"); 
 
 try 
 { 
 TESTHR(pCnn.CreateInstance(__uuidof(Connection))); 
 
 TESTHR(pRstAuthors.CreateInstance(__uuidof(Recordset))); 
 
 //If there is no ActiveConnection, you can open with defaults. 
 pRstAuthors->Open("c:\\pubs.adtg","Provider=MSPersist;", 
 adOpenForwardOnly,adLockBatchOptimistic,adCmdFile); 
 
 //Connect to the database, associate the Recordset with 
 //the connection, then update the database table with the 
 //changed Recordset. 
 pCnn->Open(strCnn,"","",NULL); 
 
 pRstAuthors->PutActiveConnection(_variant_t((IDispatch *) pCnn)); 
 pRstAuthors->UpdateBatch(adAffectAll); 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 // Pass a connection pointer accessed from the Recordset. 
 _variant_t vtConnect = pRstAuthors->GetActiveConnection(); 
 
 // GetActiveConnection returns connect string if connection 
 // is not open, else returns Connection object. 
 switch(vtConnect.vt) 
 { 
 case VT_BSTR: 
 PrintComError(e); 
 break; 
 case VT_DISPATCH: 
 PrintProviderError(vtConnect); 
 break; 
 default: 
 printf("Errors occured."); 
 break; 
 } 
 } 
 
 
 if (pRstAuthors) 
 if (pRstAuthors->State == adStateOpen) 
 pRstAuthors->Close(); 
 if (pCnn) 
 if (pCnn->State == adStateOpen) 
 pCnn->Close(); 
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
 for(long i = 0;i < nCount;i++) 
 { 
 pErr = pConnection->Errors->GetItem(i); 
 printf("Error number: %x\t%s\n", pErr->Number, 
 (LPCSTR) pErr->Description); 
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
 
 // Print COM errors. 
 printf("Error\n"); 
 printf("\tCode = %08lx\n", e.Error()); 
 printf("\tCode meaning = %s\n", e.ErrorMessage()); 
 printf("\tSource = %s\n", (LPCSTR) bstrSource); 
 printf("\tDescription = %s\n", (LPCSTR) bstrDescription); 
} 
 
bool FileExists() 
{ 
 struct _finddata_t xml_file; 
 long hFile; 
 
 if( (hFile = _findfirst("c:\\pubs.xml", &xml_file )) != -1L) 
 { 
 printf( "File already exists!\n" ); 
 return(true); 
 } 
 else 
 return (false); 
} 
// EndSaveCpp 
```

