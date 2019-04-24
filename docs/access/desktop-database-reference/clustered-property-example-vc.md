---
title: Пример использования свойства Clustered (VC++)
TOCTitle: Clustered property example (VC++)
ms:assetid: a262e38e-ce44-66cb-1adf-fad8e6b840d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249748(v=office.15)
ms:contentKeyID: 48546761
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0970fbb60d7e4c87685441ea893a44cf7ecb9cde
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296278"
---
# <a name="clustered-property-example-vc"></a>Пример использования свойства Clustered (VC++)


**Область применения**: Access 2013, Office 2013

В этом примере показано свойство [cluster](clustered-property-adox.md) [индекса](index-object-adox.md). Обратите внимание, что базы данных Microsoft Jet не поддерживают кластеризованные индексы, поэтому в этом **** примере возвращается **значение false** для свойства Clustered для всех индексов в базе данных *Northwind* .

```cpp 
 
// BeginClusteredCpp 
#import "c:\Program Files\Common Files\system\ado\msadox.dll" no_namespace 
 
#include "iostream.h" 
#include "stdio.h" 
#include "conio.h" 
 
//Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void ClusteredX(void); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 ClusteredX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// ClusteredX Function // 
// // 
////////////////////////////////////////////////////////// 
void ClusteredX() 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 _CatalogPtr m_pCatalog = NULL; 
 _TablePtr m_pTable = NULL; 
 _IndexPtr m_pIndex = NULL; 
 
 //Define other variables here 
 _variant_t vIndex; 
 try 
 { 
 TESTHR(hr = m_pCatalog.CreateInstance(__uuidof(Catalog))); 
 
 // Connect to the catalog. 
 m_pCatalog->PutActiveConnection( 
 "Provider='Microsoft.JET.OLEDB.4.0';data source=" 
 "'c:\\Program Files\\Microsoft Office\\Office\\Samples" 
 "\\Northwind.mdb';"); 
 
 int iLineCnt = 1; 
 //Enumerate Tables. 
 for(short iTable = 0;iTable < m_pCatalog->Tables->Count;iTable++) 
 { 
 vIndex = iTable; 
 m_pTable = m_pCatalog->Tables->GetItem(vIndex); 
 
 //Enumerate Indexes. 
 for(short iIndex = 0;iIndex < m_pTable->Indexes->Count; 
 iIndex++) 
 { 
 vIndex = iIndex; 
 m_pIndex = m_pTable->Indexes->GetItem(vIndex); 
 cout << m_pTable->Name << " " ; 
 cout << m_pIndex->Name << " " << (m_pIndex-> 
 GetClustered() ? "True" : "False") << endl; 
 
 if (iLineCnt%15 == 0) 
 { 
 printf("\nPress any key to continue...\n"); 
 getch(); 
 } 
 iLineCnt++; 
 } 
 } 
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
 cout << "Error occured in ClusteredX...."<< endl; 
 } 
} 
// EndClusteredCpp 
```

