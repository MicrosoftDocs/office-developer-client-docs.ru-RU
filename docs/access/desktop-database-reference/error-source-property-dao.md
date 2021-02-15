---
title: Свойство Error.Source (DAO)
TOCTitle: Source Property
ms:assetid: 3c101cac-278e-025e-55a4-8a9d1ee7db3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192677(v=office.15)
ms:contentKeyID: 48544302
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053360
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 79c5fa1e01bbb6bce4f2cef705f23f3259bf0678
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293443"
---
# <a name="errorsource-property-dao"></a><span data-ttu-id="23030-102">Свойство Error.Source (DAO)</span><span class="sxs-lookup"><span data-stu-id="23030-102">Error.Source property (DAO)</span></span>


<span data-ttu-id="23030-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="23030-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="23030-104">Возвращает имя объекта или приложения, которые изначально создали ошибку.</span><span class="sxs-lookup"><span data-stu-id="23030-104">Returns the name of the object or application that originally generated the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="23030-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23030-105">Syntax</span></span>

<span data-ttu-id="23030-106">*выражение .* Source</span><span class="sxs-lookup"><span data-stu-id="23030-106">*expression* .Source</span></span>

<span data-ttu-id="23030-107">*выражение* Переменная, представляюная объект **Error.**</span><span class="sxs-lookup"><span data-stu-id="23030-107">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="23030-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="23030-108">Remarks</span></span>

<span data-ttu-id="23030-109">Значение **свойства Source** обычно является именем класса объекта или программным кодом.</span><span class="sxs-lookup"><span data-stu-id="23030-109">The **Source** property value is usually the object's class name or programmatic ID.</span></span> <span data-ttu-id="23030-110">Используйте свойство **Source,** чтобы предоставить пользователям информацию, когда код не может обработать ошибку, созданную в объекте в другом приложении.</span><span class="sxs-lookup"><span data-stu-id="23030-110">Use the **Source** property to provide your users with information when your code is unable to handle an error generated in an object in another application.</span></span>

<span data-ttu-id="23030-111">Например, если при доступе к Microsoft Excel создается ошибка "Деление на ноль", Microsoft Excel задает **error.Number** в коде Microsoft Excel для этой ошибки и задает для свойства **Source** значение Excel.Application.</span><span class="sxs-lookup"><span data-stu-id="23030-111">For example, if you access Microsoft Excel and it generates a "Division by zero" error, Microsoft Excel sets **Error.Number** to the Microsoft Excel code for that error and sets the **Source** property to Excel.Application.</span></span> <span data-ttu-id="23030-112">Обратите внимание, что если ошибка создается в другом объекте, который называется Microsoft Excel, Microsoft Excel перехватывает ошибку и по-прежнему задает **Error.Number** в коде Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="23030-112">Note that if the error is generated in another object called by Microsoft Excel, Microsoft Excel intercepts the error and still sets **Error.Number** to the Microsoft Excel code.</span></span> <span data-ttu-id="23030-113">Однако другие свойства **объекта Error** (включая **Source)** сохраняют значения, установленные объектом, который создал ошибку.</span><span class="sxs-lookup"><span data-stu-id="23030-113">However, the other **Error** object properties (including **Source**) will retain the values as set by the object that generated the error.</span></span> <span data-ttu-id="23030-114">Свойство **Source** всегда содержит имя объекта, который изначально вызвал ошибку.</span><span class="sxs-lookup"><span data-stu-id="23030-114">The **Source** property always contains the name of the object that originally generated the error.</span></span>

<span data-ttu-id="23030-115">На основе всей документации по ошибкам можно написать код, который будет обрабатывать ошибку соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="23030-115">Based on all of the error documentation, you can write code that will handle the error appropriately.</span></span> <span data-ttu-id="23030-116">Если обработитель ошибок не удается, можно использовать сведения об объекте **[Error,](error-object-dao.md)** чтобы описать ошибку для пользователя, используя свойство **Source** и другие свойства **Error,** чтобы предоставить пользователю сведения о том, какой объект изначально вызвал ошибку, описание ошибки и так далее.</span><span class="sxs-lookup"><span data-stu-id="23030-116">If your error handler fails, you can use the **[Error](error-object-dao.md)** object information to describe the error to your user, using the **Source** property and the other **Error** properties to give the user information about which object originally caused the error, the description of the error, and so forth.</span></span>


> [!NOTE]
> <span data-ttu-id="23030-117">Конструкция **On Error Resume Next** может быть предпочтительнее, чем On Error **GoTo** при работе с ошибками, созданными при доступе к другим объектам.</span><span class="sxs-lookup"><span data-stu-id="23030-117">The **On Error Resume Next** construct may be preferable to **On Error GoTo** when dealing with errors generated during access to other objects.</span></span> <span data-ttu-id="23030-118">Проверка свойства **объекта Error** после каждого взаимодействия с объектом устраняет неоднозначность того, к каков объект, к которому был доступ код при ошибке.</span><span class="sxs-lookup"><span data-stu-id="23030-118">Checking the **Error** object property after each interaction with an object removes ambiguity about which object your code was accessing when the error occurred.</span></span> <span data-ttu-id="23030-119">Таким образом, вы можете быть уверены, какой объект поместил код ошибки в **Error.Number,** а также какой объект изначально вызвал ошибку (**Error.Source).**</span><span class="sxs-lookup"><span data-stu-id="23030-119">Thus, you can be sure which object placed the error code in **Error.Number**, as well as which object originally generated the error (**Error.Source**).</span></span>

## <a name="example"></a><span data-ttu-id="23030-120">Пример</span><span class="sxs-lookup"><span data-stu-id="23030-120">Example</span></span>

<span data-ttu-id="23030-121">В этом примере показана приодерживая ошибка, она застигает ее и отображает свойства **Description,** **Number,** **Source,** **HelpContext** и **HelpFile** итоговых объектов **Error.**</span><span class="sxs-lookup"><span data-stu-id="23030-121">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

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
