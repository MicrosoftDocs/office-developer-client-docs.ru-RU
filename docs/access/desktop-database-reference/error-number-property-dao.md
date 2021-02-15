---
title: Свойство Error.Number (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 257c403951eff5bbb2f37de8b38a1c63a3445285
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293499"
---
# <a name="errornumber-property-dao"></a><span data-ttu-id="67ab8-102">Свойство Error.Number (DAO)</span><span class="sxs-lookup"><span data-stu-id="67ab8-102">Error.Number property (DAO)</span></span>


<span data-ttu-id="67ab8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="67ab8-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="67ab8-104">Возвращает числовую величину, указываю на ошибку.</span><span class="sxs-lookup"><span data-stu-id="67ab8-104">Returns a numeric value specifying an error.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ab8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67ab8-105">Syntax</span></span>

<span data-ttu-id="67ab8-106">*выражение .* Number</span><span class="sxs-lookup"><span data-stu-id="67ab8-106">*expression* .Number</span></span>

<span data-ttu-id="67ab8-107">*выражение* Переменная, представляюная объект **Error.**</span><span class="sxs-lookup"><span data-stu-id="67ab8-107">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="67ab8-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="67ab8-108">Remarks</span></span>

<span data-ttu-id="67ab8-109">Используйте свойство **Number,** чтобы определить возникную ошибку.</span><span class="sxs-lookup"><span data-stu-id="67ab8-109">Use the **Number** property to determine the error that occurred.</span></span> <span data-ttu-id="67ab8-110">Значение свойства соответствует уникальному номеру ловушек, соответствующему условию ошибки.</span><span class="sxs-lookup"><span data-stu-id="67ab8-110">The value of the property corresponds to a unique trap number that corresponds to an error condition.</span></span>

## <a name="example"></a><span data-ttu-id="67ab8-111">Пример</span><span class="sxs-lookup"><span data-stu-id="67ab8-111">Example</span></span>

<span data-ttu-id="67ab8-112">В этом примере показана приодерживая ошибка, она застигает ее и отображает свойства **Description,** **Number,** **Source,** **HelpContext** и **HelpFile** итоговых объектов **Error.**</span><span class="sxs-lookup"><span data-stu-id="67ab8-112">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

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

