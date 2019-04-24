---
title: Свойство Error. Source (DAO)
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
# <a name="errorsource-property-dao"></a><span data-ttu-id="08f64-102">Свойство Error. Source (DAO)</span><span class="sxs-lookup"><span data-stu-id="08f64-102">Error.Source property (DAO)</span></span>


<span data-ttu-id="08f64-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="08f64-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="08f64-104">Возвращает имя объекта или приложения, которые изначально вызвали ошибку.</span><span class="sxs-lookup"><span data-stu-id="08f64-104">Returns the name of the object or application that originally generated the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="08f64-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08f64-105">Syntax</span></span>

<span data-ttu-id="08f64-106">*Expression* . Source</span><span class="sxs-lookup"><span data-stu-id="08f64-106">*expression* .Source</span></span>

<span data-ttu-id="08f64-107">*Expression (выражение* ) Переменная, представляющая объект **Error** .</span><span class="sxs-lookup"><span data-stu-id="08f64-107">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="08f64-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="08f64-108">Remarks</span></span>

<span data-ttu-id="08f64-109">Как правило, значением свойства **Source** является имя класса объекта или программный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="08f64-109">The **Source** property value is usually the object's class name or programmatic ID.</span></span> <span data-ttu-id="08f64-110">Используйте свойство **Source** , чтобы предоставить пользователям сведения о том, что код не может обработать ошибку, созданную в объекте другого приложения.</span><span class="sxs-lookup"><span data-stu-id="08f64-110">Use the **Source** property to provide your users with information when your code is unable to handle an error generated in an object in another application.</span></span>

<span data-ttu-id="08f64-111">Например, если вы обращаетесь к Microsoft Excel и создаете ошибку "деление на ноль", Microsoft Excel устанавливает **ошибку. Number** в код Microsoft Excel для этой ошибки и задает для свойства **Source** значение Excel. Application.</span><span class="sxs-lookup"><span data-stu-id="08f64-111">For example, if you access Microsoft Excel and it generates a "Division by zero" error, Microsoft Excel sets **Error.Number** to the Microsoft Excel code for that error and sets the **Source** property to Excel.Application.</span></span> <span data-ttu-id="08f64-112">Обратите внимание, что если ошибка возникает в другом объекте, вызываемом Microsoft Excel, то Microsoft Excel перехватывает ошибку, но по-прежнему задается **ошибка. Number** для кода Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="08f64-112">Note that if the error is generated in another object called by Microsoft Excel, Microsoft Excel intercepts the error and still sets **Error.Number** to the Microsoft Excel code.</span></span> <span data-ttu-id="08f64-113">Однако другие свойства объекта **Error** (включая **источник**) сохранят значения, заданные в объекте, который сформировал ошибку.</span><span class="sxs-lookup"><span data-stu-id="08f64-113">However, the other **Error** object properties (including **Source**) will retain the values as set by the object that generated the error.</span></span> <span data-ttu-id="08f64-114">Свойство **Source** всегда содержит имя объекта, который изначально создал ошибку.</span><span class="sxs-lookup"><span data-stu-id="08f64-114">The **Source** property always contains the name of the object that originally generated the error.</span></span>

<span data-ttu-id="08f64-115">На основе всей документации об ошибках можно написать код, который будет обрабатывать ошибку соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="08f64-115">Based on all of the error documentation, you can write code that will handle the error appropriately.</span></span> <span data-ttu-id="08f64-116">В случае сбоя обработчика ошибок можно использовать сведения об объекте **[Error](error-object-dao.md)** , чтобы описать ошибку для пользователя, используя свойство **Source** и другие свойства **ошибки** , чтобы предоставить пользователю сведения о том, какой объект изначально вызвал ошибка, описание ошибки и т. д.</span><span class="sxs-lookup"><span data-stu-id="08f64-116">If your error handler fails, you can use the **[Error](error-object-dao.md)** object information to describe the error to your user, using the **Source** property and the other **Error** properties to give the user information about which object originally caused the error, the description of the error, and so forth.</span></span>


> [!NOTE]
> <span data-ttu-id="08f64-117">Конструкция **On Error Resume Next** может быть предпочтительной при возникновении ошибок **goto** при возникновении ошибок, возникших во время доступа к другим объектам.</span><span class="sxs-lookup"><span data-stu-id="08f64-117">The **On Error Resume Next** construct may be preferable to **On Error GoTo** when dealing with errors generated during access to other objects.</span></span> <span data-ttu-id="08f64-118">Проверка свойства объекта **Error** после каждого взаимодействия с объектом приводит к удалению неоднозначности объекта, к которому был получен код при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="08f64-118">Checking the **Error** object property after each interaction with an object removes ambiguity about which object your code was accessing when the error occurred.</span></span> <span data-ttu-id="08f64-119">Таким образом, вы можете проверить, какой объект поместил код ошибки в **Error. Number**, а также о том, какой объект создал ошибку (**Error. Source**).</span><span class="sxs-lookup"><span data-stu-id="08f64-119">Thus, you can be sure which object placed the error code in **Error.Number**, as well as which object originally generated the error (**Error.Source**).</span></span>

## <a name="example"></a><span data-ttu-id="08f64-120">Пример</span><span class="sxs-lookup"><span data-stu-id="08f64-120">Example</span></span>

<span data-ttu-id="08f64-121">В этом примере вызывается ошибка, выполняется ее перехват и отображаются свойства **Description**, **Number**, **Source**, **HelpContext**и **HelpFile** полученного объекта **Error** .</span><span class="sxs-lookup"><span data-stu-id="08f64-121">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

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
