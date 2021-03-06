---
title: Пример использования методов GetObjectOwner и SetObjectOwner (VC++)
TOCTitle: GetObjectOwner and SetObjectOwner methods example (VC++)
ms:assetid: af38cc5c-4475-20fa-edcd-a439e1ffbf99
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249835(v=office.15)
ms:contentKeyID: 48547096
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b1227d60555dcb8da919e75bfa773fd64103a956
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292281"
---
# <a name="getobjectowner-and-setobjectowner-methods-example-vc"></a>Пример использования методов GetObjectOwner и SetObjectOwner (VC++)


**Область применения**: Access 2013, Office 2013

В этом примере демонстрируются методы [GetObjectOwner](getobjectowner-method-adox.md) и [SetObjectOwner.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox) Этот код предполагает существование учетной группы (см. приложение "Группы и пользователи", пример методов [ChangePassword (VC++),](groups-and-users-append-changepassword-methods-example-vc.md) чтобы узнать, как добавить эту группу в систему). Владелец таблицы Категорий заданной учетной таблицей.

```cpp 
 
// BeginOwnersCpp 
#import "c:\Program Files\Common Files\system\ado\msadox.dll" no_namespace 
 
#include "iostream.h" 
#include "stdio.h" 
#include "conio.h" 
 
//Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void OwnersX(void); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 OwnersX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// OwnersX Function // 
// // 
////////////////////////////////////////////////////////// 
void OwnersX() 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 _TablePtr m_pTable = NULL; 
 _CatalogPtr m_pCatalog = NULL; 
 
 try 
 { 
 TESTHR(hr = m_pCatalog.CreateInstance(__uuidof(Catalog))); 
 TESTHR(hr = m_pTable.CreateInstance(__uuidof(Table))); 
 
 //Open the Catalog. 
 m_pCatalog->PutActiveConnection( 
 "Provider='Microsoft.JET.OLEDB.4.0';" "data source='c:\\Program Files\\Microsoft Office\\" 
 "Office\\Samples\\Northwind.mdb';" 
 "jet oledb:system database='c:\\Program Files\\Microsoft Office\\" 
 "Office\\system.mdw'"); 
 
 //Print the original owner of Categories 
 _bstr_t strOwner = m_pCatalog->GetObjectOwner("Categories", 
 adPermObjTable); 
 cout << "Owner of Categories: " << strOwner << "\n" << endl; 
 int iLineCnt = 2; 
 
 //Create and append new group with a string. 
 m_pCatalog->Groups->Append("Accounting"); 
 
 //Set the owner of Categories to Accounting. 
 m_pCatalog->SetObjectOwner("Categories", 
 adPermObjTable,"Accounting"); 
 
 _variant_t vIndex; 
 //List the owners of all tables and columns in the catalog. 
 for (long iIndex = 0; iIndex < m_pCatalog->Tables->Count; iIndex++) 
 { 
 vIndex = iIndex; 
 m_pTable = m_pCatalog->Tables->GetItem(vIndex); 
 cout << "Table: " << m_pTable->Name << endl; 
 cout << " Owner: " << m_pCatalog-> 
 GetObjectOwner(m_pTable->Name,adPermObjTable) << endl; 
 if (iLineCnt%16 == 0) 
 { 
 printf("\nPress any key to continue...\n"); 
 getch(); 
 } 
 iLineCnt = iLineCnt + 2; 
 } 
 
 //Restore the original owner of Categories 
 m_pCatalog->SetObjectOwner("Categories",adPermObjTable,strOwner); 
 
 //Delete Accounting 
 m_pCatalog->Groups->Delete("Accounting"); 
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
} 
// EndOwnersCpp 
```

