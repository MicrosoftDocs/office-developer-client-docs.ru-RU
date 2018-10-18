---
<span data-ttu-id="d051f-101"><<<<<<< Название HEAD: TOCTitle примере свойство Version (VC ++): примере свойство Version (VC ++) === название: примере свойство Version (VC ++) TOCTitle: примере свойство Version (VC ++)</span><span class="sxs-lookup"><span data-stu-id="d051f-101"><<<<<<< HEAD title: Version Property Example (VC++) TOCTitle: Version Property Example (VC++) ======= title: Version property example (VC++) TOCTitle: Version property example (VC++)</span></span>
>>>>>>> <span data-ttu-id="d051f-102">главные ms:assetid: deda3998-52cd-0068-7f8c-e58c71802226 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250130(v=office.15) ms:contentKeyID: 48548201 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="d051f-102">master ms:assetid: deda3998-52cd-0068-7f8c-e58c71802226 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250130(v=office.15) ms:contentKeyID: 48548201 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="d051f-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="d051f-103"><<<<<<< HEAD</span></span>
# <a name="version-property-example-vc"></a><span data-ttu-id="d051f-104">Version Property Example (VC++)</span><span class="sxs-lookup"><span data-stu-id="d051f-104">Version Property Example (VC++)</span></span>
=======
# <a name="version-property-example-vc"></a><span data-ttu-id="d051f-105">Пример свойства версии (VC ++)</span><span class="sxs-lookup"><span data-stu-id="d051f-105">Version property example (VC++)</span></span>
>>>>>>> <span data-ttu-id="d051f-106">master</span><span class="sxs-lookup"><span data-stu-id="d051f-106">master</span></span>


<span data-ttu-id="d051f-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d051f-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d051f-108">В этом примере используется свойство [Version](version-property-ado.md) объекта [подключения](connection-object-ado.md) для отображения текущая версия ADO.</span><span class="sxs-lookup"><span data-stu-id="d051f-108">This example uses the [Version](version-property-ado.md) property of a [Connection](connection-object-ado.md) object to display the current ADO version.</span></span> <span data-ttu-id="d051f-109">Он также использует несколько динамических свойств для отображения:</span><span class="sxs-lookup"><span data-stu-id="d051f-109">It also uses several dynamic properties to show:</span></span>

  - <span data-ttu-id="d051f-110">Текущее имя СУБД и версии.</span><span class="sxs-lookup"><span data-stu-id="d051f-110">the current DBMS name and version.</span></span>

  - <span data-ttu-id="d051f-111">Версия OLE DB.</span><span class="sxs-lookup"><span data-stu-id="d051f-111">OLE DB version.</span></span>

  - <span data-ttu-id="d051f-112">Имя поставщика и версии.</span><span class="sxs-lookup"><span data-stu-id="d051f-112">provider name and version.</span></span>

  - <span data-ttu-id="d051f-113">Версия ODBC.</span><span class="sxs-lookup"><span data-stu-id="d051f-113">ODBC version.</span></span>

  - <span data-ttu-id="d051f-114">Имя драйвера ODBC и версии.</span><span class="sxs-lookup"><span data-stu-id="d051f-114">ODBC driver name and version.</span></span>

<!-- end list -->

```cpp 
 
// BeginVersionCpp 
#import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <ole2.h> 
#include <stdio.h> 
#include <conio.h> 
 
// Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void VersionX(void); 
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
 
 VersionX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// VersionX Function // 
// // 
////////////////////////////////////////////////////////// 
void VersionX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Define string variables. 
 _bstr_t strCnn("driver={SQL Server};server='MySqlServer';" 
 "user id='MyUserId';password='MyPassword';database='pubs';"); 
 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace. 
 _ConnectionPtr pConnection = NULL; 
 
 try 
 { 
 // Open connection. 
 TESTHR(pConnection.CreateInstance(__uuidof(Connection))); 
 pConnection->Open (strCnn, "", "", adConnectUnspecified); 
 
 printf("ADO Version : %s\n\n",(LPCSTR) pConnection->Version); 
 printf("DBMS Name : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("DBMS Name")->Value); 
 printf("DBMS Version : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("DBMS Version")->Value); 
 printf("OLE DB Version : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("OLE DB Version")->Value); 
 printf("Provider Name : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("Provider Name")->Value); 
 printf("Provider Version : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("Provider Version")->Value); 
 printf("Driver Name : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("Driver Name")->Value); 
 printf("Driver Version : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("Driver Version")->Value); 
 printf("Driver ODBC Version : %s\n\n",(LPCSTR) (_bstr_t) 
 pConnection->Properties->GetItem("Driver ODBC Version")->Value); 
 
 } 
 
 catch (_com_error &e) 
 { 
 // Notify the user of errors if any. 
 PrintProviderError(pConnection); 
 PrintComError(e); 
 } 
 
 if (pConnection) 
 if (pConnection->State == adStateOpen) 
 pConnection->Close(); 
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
// EndVersionCpp 
```

