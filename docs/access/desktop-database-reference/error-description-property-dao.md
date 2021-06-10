---
title: Свойство Error.Description (DAO)
TOCTitle: Description Property
ms:assetid: 47a84bec-3258-f2c7-e1af-239da39844dc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193218(v=office.15)
ms:contentKeyID: 48544601
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053358
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 1d7e949771e764c22e93ef56059930ccf39584ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293506"
---
# <a name="errordescription-property-dao"></a><span data-ttu-id="371b1-102">Свойство Error.Description (DAO)</span><span class="sxs-lookup"><span data-stu-id="371b1-102">Error.Description property (DAO)</span></span>


<span data-ttu-id="371b1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="371b1-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="371b1-104">Возвращает дескриптивную строку, связанную с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="371b1-104">Returns a descriptive string associated with an error.</span></span> <span data-ttu-id="371b1-105">Это свойство по умолчанию для объекта **Error.**</span><span class="sxs-lookup"><span data-stu-id="371b1-105">This is the default property for the **Error** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="371b1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="371b1-106">Syntax</span></span>

<span data-ttu-id="371b1-107">*выражения* . Описание</span><span class="sxs-lookup"><span data-stu-id="371b1-107">*expression* .Description</span></span>

<span data-ttu-id="371b1-108">*выражение* Переменная, представляюная объект **Error.**</span><span class="sxs-lookup"><span data-stu-id="371b1-108">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="371b1-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="371b1-109">Remarks</span></span>

<span data-ttu-id="371b1-110">Свойство **Description** содержит краткое описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="371b1-110">The **Description** property comprises a short description of the error.</span></span> <span data-ttu-id="371b1-111">Используйте это свойство, чтобы предупредить пользователя об ошибке, которую нельзя или не хотите обрабатывать.</span><span class="sxs-lookup"><span data-stu-id="371b1-111">Use this property to alert the user about an error that you cannot or do not want to handle.</span></span>

## <a name="example"></a><span data-ttu-id="371b1-112">Пример</span><span class="sxs-lookup"><span data-stu-id="371b1-112">Example</span></span>

<span data-ttu-id="371b1-113">В этом примере приводится ошибка, она ловушек, и отображает описание **,** номер **,** **источник**, **HelpContext** и **HelpFile** свойства в результате объекта Ошибки.</span><span class="sxs-lookup"><span data-stu-id="371b1-113">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting Error object.</span></span>

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

