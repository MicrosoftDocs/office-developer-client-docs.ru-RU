---
title: Пример использования свойства Type (Property) (VB)
TOCTitle: Type property example (Property) (VB)
ms:assetid: b3fecd24-e15a-3216-e2c8-0f4ce5655b9c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249858(v=office.15)
ms:contentKeyID: 48547209
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 56e47b32bb85da237464842dcb049092750d77a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306274"
---
# <a name="type-property-example-property-vb"></a><span data-ttu-id="1d928-102">Пример использования свойства Type (Property) (VB)</span><span class="sxs-lookup"><span data-stu-id="1d928-102">Type property example (Property) (VB)</span></span>


<span data-ttu-id="1d928-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d928-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d928-104">В этом примере [демонстрируется свойство Type.](type-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="1d928-104">This example demonstrates the [Type](type-property-ado.md) property.</span></span> <span data-ttu-id="1d928-105">Это модель утилиты для перечисления имен и типов коллекции, таких как [свойства,](properties-collection-ado.md) [поля](fields-collection-ado.md)и т.д.</span><span class="sxs-lookup"><span data-stu-id="1d928-105">It is a model of a utility for listing the names and types of a collection, like [Properties](properties-collection-ado.md), [Fields](fields-collection-ado.md), etc.</span></span>

<span data-ttu-id="1d928-106">Нам не нужно открывать набор [Recordset для](recordset-object-ado.md) доступа к его коллекции **свойств;** они в жизнь, когда **объект Recordset** мгновенно.</span><span class="sxs-lookup"><span data-stu-id="1d928-106">We do not need to open the [Recordset](recordset-object-ado.md) to access its **Properties** collection; they come into existence when the **Recordset** object is instantiated.</span></span> <span data-ttu-id="1d928-107">Однако настройка свойства [CursorLocation](cursorlocation-property-ado.md) в **adUseClient** добавляет несколько динамических  свойств в коллекцию свойств объекта **Recordset,** что делает пример немного более интересным.</span><span class="sxs-lookup"><span data-stu-id="1d928-107">However, setting the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient** adds several dynamic properties to the **Recordset** object's **Properties** collection, making the example a little more interesting.</span></span> <span data-ttu-id="1d928-108">Для иллюстрации мы явно используем свойство [Item](item-property-ado.md) для доступа к каждому [объекту Property.](property-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="1d928-108">For sake of illustration, we explicitly use the [Item](item-property-ado.md) property to access each [Property](property-object-ado.md) object.</span></span>

```vb 
 
'BeginTypePropertyVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' recordset variables 
 Dim rst As ADODB.Recordset 
 Dim prop As ADODB.Property 
 ' property variables 
 Dim ix As Integer 
 Dim strMsg As String 
 
 ' create client-side recordset 
 Set rst = New ADODB.Recordset 
 rst.CursorLocation = adUseClient 
 ' enumerate property types 
 For ix = 0 To rst.Properties.Count - 1 
 Set prop = rst.Properties.Item(ix) 
 Select Case prop.Type 
 Case adBigInt 
 strMsg = "adBigInt" 
 Case adBinary 
 strMsg = "adBinary" 
 Case adBoolean 
 strMsg = "adBoolean" 
 Case adBSTR 
 strMsg = "adBSTR" 
 Case adChapter 
 strMsg = "adChapter" 
 Case adChar 
 strMsg = "adChar" 
 Case adCurrency 
 strMsg = "adCurrency" 
 Case adDate 
 strMsg = "adDate" 
 Case adDBDate 
 strMsg = "adDBDate" 
 Case adDBTime 
 strMsg = "adDBTime" 
 Case adDBTimeStamp 
 strMsg = "adDBTimeStamp" 
 Case adDecimal 
 strMsg = "adDecimal" 
 Case adDouble 
 strMsg = "adDouble" 
 Case adEmpty 
 strMsg = "adEmpty" 
 Case adError 
 strMsg = "adError" 
 Case adFileTime 
 strMsg = "adFileTime" 
 Case adGUID 
 strMsg = "adGUID" 
 Case adIDispatch 
 strMsg = "adIDispatch" 
 Case adInteger 
 strMsg = "adInteger" 
 Case adIUnknown 
 strMsg = "adIUnknown" 
 Case adLongVarBinary 
 strMsg = "adLongVarBinary" 
 Case adLongVarChar 
 strMsg = "adLongVarChar" 
 Case adLongVarWChar 
 strMsg = "adLongVarWChar" 
 Case adNumeric 
 strMsg = "adNumeric" 
 Case adPropVariant 
 strMsg = "adPropVariant" 
 Case adSingle 
 strMsg = "adSingle" 
 Case adSmallInt 
 strMsg = "adSmallInt" 
 Case adTinyInt 
 strMsg = "adTinyInt" 
 Case adUnsignedBigInt 
 strMsg = "adUnsignedBigInt" 
 Case adUnsignedInt 
 strMsg = "adUnsignedInt" 
 Case adUnsignedSmallInt 
 strMsg = "adUnsignedSmallInt" 
 Case adUnsignedTinyInt 
 strMsg = "adUnsignedTinyInt" 
 Case adUserDefined 
 strMsg = "adUserDefined" 
 Case adVarBinary 
 strMsg = "adVarBinary" 
 Case adVarChar 
 strMsg = "adVarChar" 
 Case adVariant 
 strMsg = "adVariant" 
 Case adVarNumeric 
 strMsg = "adVarNumeric" 
 Case adVarWChar 
 strMsg = "adVarWChar" 
 Case adWChar 
 strMsg = "adWChar" 
 Case Else 
 strMsg = "*UNKNOWN*" 
 End Select 
 'show results 
 Debug.Print "Property " & ix & ": " & prop.Name & _ 
 ", Type = " & strMsg 
 Next ix 
 
 ' clean up 
 Set rst = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 Set rst = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
'EndTypePropertyVB 
```

