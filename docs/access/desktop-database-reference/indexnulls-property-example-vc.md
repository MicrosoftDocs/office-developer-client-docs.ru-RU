---
title: IndexNulls Property Example (VC++)
TOCTitle: IndexNulls Property Example (VC++)
ms:assetid: 05d1f8b3-ae70-cca5-d60d-af55f5f7c13a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248813(v=office.15)
ms:contentKeyID: 48543039
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28e0c1e1f7fb92f5e6752f732c275fff609252d3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482070"
---
# <a name="indexnulls-property-example-vc"></a><span data-ttu-id="5ba9f-102">IndexNulls Property Example (VC++)</span><span class="sxs-lookup"><span data-stu-id="5ba9f-102">IndexNulls Property Example (VC++)</span></span>


<span data-ttu-id="5ba9f-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5ba9f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5ba9f-104">В этом примере демонстрируется свойство [IndexNulls](indexnulls-property-adox.md) [индекса](index-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="5ba9f-104">This example demonstrates the [IndexNulls](indexnulls-property-adox.md) property of an [Index](index-object-adox.md).</span></span> <span data-ttu-id="5ba9f-105">Код создает новый индекс и задает значение **IndexNulls** зависимости от введенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="5ba9f-105">The code creates a new index and sets the value of **IndexNulls** based on user input.</span></span> <span data-ttu-id="5ba9f-106">Затем **индекс** добавляется **сотрудников** [в таблице](table-object-adox.md) в [каталог](catalog-object-adox.md) *"Борей"* .</span><span class="sxs-lookup"><span data-stu-id="5ba9f-106">Then, the **Index** is appended to the **Employees** [Table](table-object-adox.md) in the *Northwind* [Catalog](catalog-object-adox.md).</span></span> <span data-ttu-id="5ba9f-107">Новый **индекс** применяется к [набору записей](recordset-object-ado.md) , основанного на таблице **Employees** и открывается **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="5ba9f-107">The new **Index** is applied to a [Recordset](recordset-object-ado.md) based on the **Employees** table, and the **Recordset** is opened.</span></span> <span data-ttu-id="5ba9f-108">Новая запись добавляется к таблице **Employees** **нулевое** значение в индексированных полей.</span><span class="sxs-lookup"><span data-stu-id="5ba9f-108">A new record is added to the **Employees** table, with a **Null** value in the indexed field.</span></span> <span data-ttu-id="5ba9f-109">Отображение этой новой записи зависит от значения свойства **IndexNulls** .</span><span class="sxs-lookup"><span data-stu-id="5ba9f-109">Whether this new record is displayed depends on the setting of the **IndexNulls** property.</span></span>

```cpp 
 
// BeignIndexNullCpp 
#import "C:\Program Files\Common Files\System\ADO\msado15.dll" rename("EOF", "EndOfFile") 
#import "c:\Program Files\Common Files\system\ado\msadox.dll" no_namespace 
 
#include "iostream.h" 
#include "stdio.h" 
#include "conio.h" 
#include "ADOXIndexNullsX.h" 
 
// Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void IndexNullsX(_bstr_t); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 printf("\nShow records having indexed field value = NULL? (Y/N):"); 
 char input = getche(); 
 
 if(toupper(input)=='Y') 
 { 
 IndexNullsX("Allow"); 
 } 
 else if(toupper(input)=='N') 
 { 
 IndexNullsX("Ignore"); 
 } 
 else 
 { 
 exit(0); 
 } 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// IndexNullsX Function // 
// // 
////////////////////////////////////////////////////////// 
void IndexNullsX(_bstr_t strSel) 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 _CatalogPtr m_pCatalog = NULL; 
 _IndexPtr m_pIndexNew = NULL; 
 
 // Define ADODB object pointers 
 ADODB::_ConnectionPtr m_pCnn = NULL; 
 ADODB::_RecordsetPtr m_pRstEmployees = NULL; 
 
 // Define other variables 
 IADORecordBinding *picRs = NULL; // Interface Pointer Declared 
 CEmployeeRs emprs; // C++ Class Object 
 
 // Define string variable. 
 _bstr_t strCnn("Provider='Microsoft.JET.OLEDB.4.0';" 
 "data source='c:\\Program Files\\Microsoft Office\\Office\\" 
 "Samples\\Northwind.mdb';"); 
 
 try 
 { 
 TESTHR(hr = m_pCnn.CreateInstance(__uuidof(ADODB::Connection))); 
 TESTHR(hr = m_pCatalog.CreateInstance(__uuidof (Catalog))); 
 TESTHR(hr = m_pIndexNew.CreateInstance(__uuidof(Index))); 
 TESTHR(hr = m_pRstEmployees.CreateInstance( 
 __uuidof(ADODB::Recordset))); 
 
 // Connect the catalog. 
 m_pCnn->Open(strCnn,"","",NULL); 
 m_pCatalog->PutActiveConnection(_variant_t((IDispatch *)m_pCnn)); 
 
 // Append Country column to new index. 
 m_pIndexNew->Columns->Append("Country",adVarWChar,0); 
 m_pIndexNew->Name = "NewIndex"; 
 
 // Set IndexNulls based on user input 
 if(strcmp((LPSTR)strSel,"Allow")==0) 
 { 
 m_pIndexNew->IndexNulls = adIndexNullsAllow; 
 } 
 else if(strcmp((LPSTR)strSel,"Ignore")==0) 
 { 
 m_pIndexNew->IndexNulls = adIndexNullsIgnore; 
 } 
 
 // Append new index to Employees table 
 m_pCatalog->Tables->GetItem("Employees")->Indexes->Append( 
 _variant_t((IDispatch *)m_pIndexNew)); 
 m_pRstEmployees->Index = m_pIndexNew->Name; 
 m_pRstEmployees->Open("Employees", 
 _variant_t((IDispatch *)m_pCnn), 
 ADODB::adOpenKeyset,ADODB::adLockOptimistic, 
 ADODB::adCmdTableDirect); 
 
 // Add a new record to the Employees table. 
 m_pRstEmployees->AddNew(); 
 m_pRstEmployees->Fields->GetItem("FirstName")->Value = 
 (_bstr_t) "Gary"; 
 m_pRstEmployees->Fields->GetItem("LastName")->Value = 
 (_bstr_t) "Haarsager"; 
 m_pRstEmployees->Update(); 
 
 // Bookmark the newly added record. 
 _variant_t varBookmark = m_pRstEmployees->Bookmark; 
 
 // Use the new index to set the order of the records. 
 m_pRstEmployees->MoveFirst(); 
 printf("\n\nIndex = %s,",(LPSTR) m_pRstEmployees->Index); 
 printf("IndexNulls = %d\n\n",m_pIndexNew->IndexNulls); 
 cout<<"Country - Name"<<endl; 
 
 // Open an IADORecordBinding interface pointer which 
 // we will use for binding Recordset to a class 
 TESTHR(hr = m_pRstEmployees->QueryInterface( 
 __uuidof(IADORecordBinding),(LPVOID*)&picRs)); 
 
 // Bind the Recordset to a C++ class here 
 TESTHR(hr = picRs->BindToRecordset(&emprs)); 
 
 // Enumerate the Recordset.The value of the 
 // IndexNulls property will determine if the newly 
 // added record appears in the output. 
 while(!(m_pRstEmployees->EndOfFile)) 
 { 
 printf("%s - %s %s\n", 
 emprs.lemp_CountryStatus == adFldOK ? 
 emprs.m_szemp_Country :"[Null]", 
 emprs.lemp_FirstNameStatus == adFldOK ? 
 emprs.m_szemp_FirstName :"<NULL>", 
 emprs.lemp_LastNameStatus == adFldOK ? 
 emprs.m_szemp_LastName :"<NULL>"); 
 m_pRstEmployees->MoveNext(); 
 } 
 
 // Delete new record because this is a demonstration. 
 m_pRstEmployees->Bookmark = varBookmark; 
 m_pRstEmployees->Delete(ADODB::adAffectCurrent); 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 _bstr_t bstrSource(e.Source()); 
 _bstr_t bstrDescription(e.Description()); 
 
 printf("\n\tSource : %s \n\tdescription : %s \n ", 
 (LPCSTR)bstrSource,(LPCSTR)bstrDescription); 
 } 
 catch(...) 
 { 
 cout << "Error occured in include files...."<< endl; 
 } 
 
 if (m_pRstEmployees) 
 { 
 if (m_pRstEmployees->State == 1) 
 { 
 m_pRstEmployees->Close(); 
 m_pRstEmployees = NULL; 
 } 
 } 
 
 // Delete new Index because this is a demonstration. 
 if (m_pCatalog) 
 m_pCatalog->Tables->GetItem("Employees")->Indexes-> 
 Delete(m_pIndexNew->Name); 
 
 if (m_pCnn) 
 { 
 if (m_pCnn->State == 1) 
 { 
 m_pCnn->Close(); 
 m_pCnn = NULL; 
 } 
 } 
 
 m_pCatalog = NULL; 
} 
// EndIndexNullCpp 
```

<br/>

<span data-ttu-id="5ba9f-110">**IndexNullX.h**</span><span class="sxs-lookup"><span data-stu-id="5ba9f-110">**IndexNullX.h**</span></span>

```cpp
    // BeginIndexNullsH 
    // IndexNullsX.h 
     
    #include "icrsint.h" 
     
    //This class extracts LastName,Country,FirstName from Employees table 
     
    class CEmployeeRs : public CADORecordBinding 
    { 
    BEGIN_ADO_BINDING(CEmployeeRs) 
     // Column LastName is the 2nd field in the table 
     ADO_VARIABLE_LENGTH_ENTRY2(2,adVarChar,m_szemp_LastName, 
     sizeof(m_szemp_LastName),lemp_LastNameStatus,TRUE) 
     // Column Country is the 11th field in the table 
     ADO_VARIABLE_LENGTH_ENTRY2(11,adVarChar,m_szemp_Country, 
     sizeof(m_szemp_Country),lemp_CountryStatus,TRUE) 
     // Column Country is the 17th field in the table 
     ADO_VARIABLE_LENGTH_ENTRY2(17,adVarChar,m_szemp_FirstName, 
     sizeof(m_szemp_FirstName),lemp_FirstNameStatus,TRUE) 
    END_ADO_BINDING() 
     
    public: 
     CHAR m_szemp_LastName[21]; 
     ULONG lemp_LastNameStatus; 
     CHAR m_szemp_Country[16]; 
     ULONG lemp_CountryStatus; 
     CHAR m_szemp_FirstName[11]; 
     ULONG lemp_FirstNameStatus; 
    }; 
    // EndIndexNullsH
```
