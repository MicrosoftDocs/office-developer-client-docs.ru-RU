---
title: Error.Number Property (DAO)
TOCTitle: Number Property
ms:assetid: 2fb94dca-f990-04f8-bbd2-9919d28de75a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192259(v=office.15)
ms:contentKeyID: 48544013
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053363
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8e7f5f4b6a0d4fa12be35a20f0a17717fdef1062
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480226"
---
# <a name="errornumber-property-dao"></a><span data-ttu-id="bad0f-102">Error.Number Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="bad0f-102">Error.Number Property (DAO)</span></span>


<span data-ttu-id="bad0f-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bad0f-103">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="bad0f-104">Возвращает значение, указывающее ошибку.</span><span class="sxs-lookup"><span data-stu-id="bad0f-104">Returns a numeric value specifying an error.</span></span>

## <a name="syntax"></a><span data-ttu-id="bad0f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bad0f-105">Syntax</span></span>

<span data-ttu-id="bad0f-106">*выражение* . Номер</span><span class="sxs-lookup"><span data-stu-id="bad0f-106">*expression* .Number</span></span>

<span data-ttu-id="bad0f-107">*выражение* Переменная, которая содержит объект **Error** .</span><span class="sxs-lookup"><span data-stu-id="bad0f-107">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bad0f-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="bad0f-108">Remarks</span></span>

<span data-ttu-id="bad0f-109">Используйте свойство **номер** для определения возникшей ошибки.</span><span class="sxs-lookup"><span data-stu-id="bad0f-109">Use the **Number** property to determine the error that occurred.</span></span> <span data-ttu-id="bad0f-110">Значение свойства соответствует выполнилось уникальный номер, который соответствует ошибки.</span><span class="sxs-lookup"><span data-stu-id="bad0f-110">The value of the property corresponds to a unique trap number that corresponds to an error condition.</span></span>

## <a name="example"></a><span data-ttu-id="bad0f-111">Пример</span><span class="sxs-lookup"><span data-stu-id="bad0f-111">Example</span></span>

<span data-ttu-id="bad0f-112">В этом примере принудительно ошибку, его перехватывает и отображает свойства **Description**, **номер**, **источник**, **HelpContext**и **HelpFile** итоговый объект **Error** .</span><span class="sxs-lookup"><span data-stu-id="bad0f-112">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

```vb 
Sub DescriptionX() 
 
 Dim dbsTest As Database 
 
 On Error GoTo ErrorHandler 
 
 ' Intentionally trigger an error. 
 Set dbsTest = OpenDatabase("NoDatabase") 
 
 Exit Sub 
 
ErrorHandler: 
 Dim strError As String 
 Dim errLoop As Error 
 
 ' Enumerate Errors collection and display properties of 
 ' each Error object. 
 For Each errLoop In Errors 
 With errLoop 
 strError = _ 
 "Error #" & .Number & vbCr 
 strError = strError & _ 
 " " & .Description & vbCr 
 strError = strError & _ 
 " (Source: " & .Source & ")" & vbCr 
 strError = strError & _ 
 "Press F1 to see topic " & .HelpContext & vbCr 
 strError = strError & _ 
 " in the file " & .HelpFile & "." 
 End With 
 MsgBox strError 
 Next 
 
 Resume Next 
 
End Sub 
 
```

