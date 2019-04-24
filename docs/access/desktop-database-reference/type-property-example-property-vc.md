---
title: Пример использования свойства Type (Property) (VC++)
TOCTitle: Type property example (Property) (VC++)
ms:assetid: ddf0233f-585e-6659-7fd6-f924f3a31f21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250122(v=office.15)
ms:contentKeyID: 48548168
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7a92b5380837668df6661d1d88eb8bb0bd2cb4ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313967"
---
# <a name="type-property-example-property-vc"></a>Пример использования свойства Type (Property) (VC++)


**Область применения**: Access 2013, Office 2013

В этом примере показано свойство [Type](type-property-ado.md) . Это модель служебной программы для перечисления имен и типов коллекции, таких как [Свойства](properties-collection-ado.md), [поля](fields-collection-ado.md)и т. д.

Чтобы получить доступ к коллекции **свойств** , не нужно открывать этот [набор записей](recordset-object-ado.md) . они приходят на существование при создании экземпляра объекта **Recordset** . Тем не менее, установка свойства [CursorLocation](cursorlocation-property-ado.md) равным **адусеклиент** добавляет несколько динамических свойств в коллекцию **свойств** объекта **Recordset** , делая пример более интересным. Для наглядности мы явно используем свойство [Item](item-property-ado.md) для доступа к каждому объекту [Property](property-object-ado.md) .

```cpp 
 
// BeginTypePropertyCpp 
#import "C:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <ole2.h> 
#include <stdio.h> 
#include<conio.h> 
 
// Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void TypeX(); 
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
 
 TypeX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// TypeX Function // 
// // 
////////////////////////////////////////////////////////// 
void TypeX() 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace 
 _RecordsetPtr pRst = NULL; 
 PropertyPtr pProperty = NULL; 
 
 //Define Other Variables 
 _bstr_t strMsg; 
 _variant_t vIndex; 
 int intLineCnt = 0; 
 
 try 
 { 
 TESTHR(pRst.CreateInstance (__uuidof(Recordset))); 
 
 // Set the Recordset Cursor Location 
 pRst->CursorLocation = adUseClient; 
 
 for (short iIndex = 0; iIndex <= (pRst->Properties-> 
 GetCount() - 1);iIndex++) 
 { 
 vIndex = iIndex; 
 pProperty = pRst->Properties->GetItem(vIndex); 
 
 int propType = (int)pProperty->GetType(); 
 switch(propType) 
 { 
 case adBigInt: 
 strMsg = "adBigInt"; 
 break; 
 case adBinary: 
 strMsg = "adBinary"; 
 break; 
 case adBoolean: 
 strMsg = "adBoolean"; 
 break; 
 case adBSTR: 
 strMsg = "adBSTR"; 
 break; 
 case adChapter: 
 strMsg = "adChapter"; 
 break; 
 case adChar: 
 strMsg = "adChar"; 
 break; 
 case adCurrency: 
 strMsg = "adCurrency"; 
 break; 
 case adDate: 
 strMsg = "adDate"; 
 break; 
 case adDBDate: 
 strMsg = "adDBDate"; 
 break; 
 case adDBTime: 
 strMsg = "adDBTime"; 
 break; 
 case adDBTimeStamp: 
 strMsg = "adDBTimeStamp"; 
 break; 
 case adDecimal: 
 strMsg = "adDecimal"; 
 break; 
 case adDouble: 
 strMsg = "adDouble"; 
 break; 
 case adEmpty: 
 strMsg = "adEmpty"; 
 break; 
 case adError: 
 strMsg = "adError"; 
 break; 
 case adFileTime: 
 strMsg = "adFileTime"; 
 break; 
 case adGUID: 
 strMsg = "adGUID"; 
 break; 
 case adIDispatch: 
 strMsg = "adIDispatch"; 
 break; 
 case adInteger: 
 strMsg = "adInteger"; 
 break; 
 case adIUnknown: 
 strMsg = "adIUnknown"; 
 break; 
 case adLongVarBinary: 
 strMsg = "adLongVarBinary"; 
 break; 
 case adLongVarChar: 
 strMsg = "adLongVarChar"; 
 break; 
 case adLongVarWChar: 
 strMsg = "adLongVarWChar"; 
 break; 
 case adNumeric: 
 strMsg = "adNumeric"; 
 break; 
 case adPropVariant: 
 strMsg = "adPropVariant"; 
 break; 
 case adSingle: 
 strMsg = "adSingle"; 
 break; 
 case adSmallInt: 
 strMsg = "adSmallInt"; 
 break; 
 case adTinyInt: 
 strMsg = "adTinyInt"; 
 break; 
 case adUnsignedBigInt: 
 strMsg = "adUnsignedBigInt"; 
 break; 
 case adUnsignedInt: 
 strMsg = "adUnsignedInt"; 
 break; 
 case adUnsignedSmallInt: 
 strMsg = "adUnsignedSmallInt"; 
 break; 
 case adUnsignedTinyInt: 
 strMsg = "adUnsignedTinyInt"; 
 break; 
 case adUserDefined: 
 strMsg = "adUserDefined"; 
 break; 
 case adVarBinary: 
 strMsg = "adVarBinary"; 
 break; 
 case adVarChar: 
 strMsg = "adVarChar"; 
 break; 
 case adVariant: 
 strMsg = "adVariant"; 
 break; 
 case adVarNumeric: 
 strMsg = "adVarNumeric"; 
 break; 
 case adVarWChar: 
 strMsg = "adVarWChar"; 
 break; 
 case adWChar: 
 strMsg = "adWChar"; 
 break; 
 default: 
 strMsg = "*UNKNOWN*"; 
 break; 
 } 
 
 intLineCnt++; 
 if (intLineCnt%20 == 0) 
 { 
 printf("\nPress any key to continue...\n"); 
 getch(); 
 } 
 printf ("Property %d : %s,Type = %s\n",iIndex, 
 (LPCSTR)pProperty->GetName(),(LPCSTR)strMsg); 
 } 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 PrintComError(e); 
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
// EndTypePropertyCpp 
```

