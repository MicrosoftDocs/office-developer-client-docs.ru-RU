---
title: Пример использования свойства ParentCatalog (VC++)
TOCTitle: ParentCatalog property example (VC++)
ms:assetid: fad6574f-698f-f48a-ba0b-59f048ae012c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250281(v=office.15)
ms:contentKeyID: 48548855
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3e879df56cbf3c35aae67ece0e4c464bc7587e63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287771"
---
# <a name="parentcatalog-property-example-vc"></a><span data-ttu-id="06f09-102">Пример использования свойства ParentCatalog (VC++)</span><span class="sxs-lookup"><span data-stu-id="06f09-102">ParentCatalog property example (VC++)</span></span>


<span data-ttu-id="06f09-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="06f09-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="06f09-104">В приведенном ниже коде показано, как использовать свойство [ParentCatalog](parentcatalog-property-adox.md) для доступа к свойству, зависящему от поставщика, перед добавлением таблицы в каталог.</span><span class="sxs-lookup"><span data-stu-id="06f09-104">The following code demonstrates how to use the [ParentCatalog](parentcatalog-property-adox.md) property to access a provider-specific property prior to appending a table to a catalog.</span></span> <span data-ttu-id="06f09-105">Свойство имеет автоПриращение, которое создает поле AutoIncrement в базе данных Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="06f09-105">The property is AutoIncrement, which creates an AutoIncrement field in a Microsoft Jet database.</span></span>

```cpp 
 
// BeginCreateAutoIncrColumnCpp 
#import "c:\Program Files\Common Files\system\ado\msadox.dll" no_namespace 
#import "c:\Program Files\Common Files\system\ado\msado15.dll" 
 
#include "iostream.h" 
#include "stdio.h" 
#include "conio.h" 
 
//Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void CreateAutoIncrColumnX(void); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 CreateAutoIncrColumnX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// CreateAutoIncrColumnX Function // 
// // 
////////////////////////////////////////////////////////// 
void CreateAutoIncrColumnX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 _CatalogPtr m_pCatalog = NULL; 
 _TablePtr m_pTable = NULL; 
 
 // Define ADODB object pointers. 
 ADODB::_ConnectionPtr m_pCnn = NULL; 
 
 //Define string variables 
 _bstr_t strCnn("Provider='Microsoft.JET.OLEDB.4.0';" 
 "Data Source='c:\\Program Files\\Microsoft Office\\" 
 "Office\\Samples\\Northwind.mdb';"); 
 try 
 { 
 TESTHR(hr = m_pCnn.CreateInstance(__uuidof(ADODB::Connection))); 
 
 TESTHR(hr = m_pCatalog.CreateInstance(__uuidof (Catalog))); 
 
 TESTHR(hr = m_pTable.CreateInstance(__uuidof (Table))); 
 
 // Connect the catalog. 
 m_pCnn->Open (strCnn, "", "", NULL); 
 
 m_pCatalog->PutActiveConnection(variant_t((IDispatch *)m_pCnn)); 
 
 m_pTable->Name="MyContacts"; 
 m_pTable->ParentCatalog = m_pCatalog; 
 
 // Create fields and append them to the new Table object. 
 m_pTable->Columns->Append("ContactId", adInteger,0); 
 
 // Make the ContactId column and auto incrementing column 
 m_pTable->Columns->GetItem("ContactId")->Properties-> 
 GetItem("AutoIncrement")->Value = true; 
 m_pTable->Columns->Append("CustomerID", adVarWChar,0); 
 m_pTable->Columns->Append("FirstName", adVarWChar,0); 
 m_pTable->Columns->Append("LastName", adVarWChar,0); 
 m_pTable->Columns->Append("Phone", adVarWChar, 20); 
 m_pTable->Columns->Append("Notes", adLongVarWChar,0); 
 m_pCatalog->Tables->Append(_variant_t((IDispatch*)m_pTable)); 
 
 // Refresh the database. 
 m_pCatalog->Tables->Refresh(); 
 
 printf("Table 'MyContacts' is added.\n"); 
 
 // Delete new table, since this is only an example 
 m_pCatalog->Tables->Delete("MyContacts"); 
 
 printf("Table 'MyContacts' is deleted.\n"); 
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
 cout << "Error occured in CreateAutoIncrColumnX...."<< endl; 
 } 
 
 m_pCatalog = NULL; 
} 
// EndCreateAutoIncrColumnCpp 
```

