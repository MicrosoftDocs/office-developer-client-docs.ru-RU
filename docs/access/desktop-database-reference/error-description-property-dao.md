---
title: Error.Description Property (DAO)
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
ms.openlocfilehash: 2de4c87832956fb690f67f734d418a855b179d8c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870340"
---
# <a name="errordescription-property-dao"></a><span data-ttu-id="54c5a-102">Error.Description Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="54c5a-102">Error.Description Property (DAO)</span></span>


<span data-ttu-id="54c5a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="54c5a-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="54c5a-104">Возвращает строку описания, связанную с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="54c5a-104">Returns a descriptive string associated with an error.</span></span> <span data-ttu-id="54c5a-105">Это свойство по умолчанию для объект **Error** .</span><span class="sxs-lookup"><span data-stu-id="54c5a-105">This is the default property for the **Error** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="54c5a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54c5a-106">Syntax</span></span>

<span data-ttu-id="54c5a-107">*выражение* . Описание</span><span class="sxs-lookup"><span data-stu-id="54c5a-107">*expression* .Description</span></span>

<span data-ttu-id="54c5a-108">*выражение* Переменная, которая содержит объект **Error** .</span><span class="sxs-lookup"><span data-stu-id="54c5a-108">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="54c5a-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="54c5a-109">Remarks</span></span>

<span data-ttu-id="54c5a-110">Свойство **Description** содержит краткое описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="54c5a-110">The **Description** property comprises a short description of the error.</span></span> <span data-ttu-id="54c5a-111">Это свойство используется для предупреждения об ошибке, не могут и не хотите обрабатывать.</span><span class="sxs-lookup"><span data-stu-id="54c5a-111">Use this property to alert the user about an error that you cannot or do not want to handle.</span></span>

## <a name="example"></a><span data-ttu-id="54c5a-112">Пример</span><span class="sxs-lookup"><span data-stu-id="54c5a-112">Example</span></span>

<span data-ttu-id="54c5a-113">В этом примере принудительно ошибку, его перехватывает и отображает свойства **Description**, **номер**, **источник**, **HelpContext**и **HelpFile** итоговый объект Error.</span><span class="sxs-lookup"><span data-stu-id="54c5a-113">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting Error object.</span></span>

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

