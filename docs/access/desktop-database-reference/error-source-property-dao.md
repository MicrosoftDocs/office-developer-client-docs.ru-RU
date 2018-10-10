---
title: Error.Source Property (DAO)
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
ms.openlocfilehash: b9aafe1b16b3d989a81ff21f97bd4b6d10f79de3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482036"
---
# <a name="errorsource-property-dao"></a><span data-ttu-id="857fa-102">Error.Source Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="857fa-102">Error.Source Property (DAO)</span></span>


<span data-ttu-id="857fa-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="857fa-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="857fa-104">Возвращает имя объекта или приложения, вызвавшего ошибку.</span><span class="sxs-lookup"><span data-stu-id="857fa-104">Returns the name of the object or application that originally generated the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="857fa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="857fa-105">Syntax</span></span>

<span data-ttu-id="857fa-106">*выражение* . Источник</span><span class="sxs-lookup"><span data-stu-id="857fa-106">*expression* .Source</span></span>

<span data-ttu-id="857fa-107">*выражение* Переменная, которая содержит объект **Error** .</span><span class="sxs-lookup"><span data-stu-id="857fa-107">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="857fa-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="857fa-108">Remarks</span></span>

<span data-ttu-id="857fa-109">Значение свойства **источника** обычно является именем класса объекта или программный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="857fa-109">The **Source** property value is usually the object's class name or programmatic ID.</span></span> <span data-ttu-id="857fa-110">Используйте свойство **Source** для предоставления пользователям со сведениями, если код не может обработать ошибку, созданную в объект в другом приложении.</span><span class="sxs-lookup"><span data-stu-id="857fa-110">Use the **Source** property to provide your users with information when your code is unable to handle an error generated in an object in another application.</span></span>

<span data-ttu-id="857fa-111">Например если доступ к Microsoft Excel, и возникает ошибка «Деление на ноль», Microsoft Excel показана **Error.Number** в код Microsoft Excel для этой ошибки и свойство **Source** на Excel.Application.</span><span class="sxs-lookup"><span data-stu-id="857fa-111">For example, if you access Microsoft Excel and it generates a "Division by zero" error, Microsoft Excel sets **Error.Number** to the Microsoft Excel code for that error and sets the **Source** property to Excel.Application.</span></span> <span data-ttu-id="857fa-112">Обратите внимание на то, что, если ошибка возникает в другой объект с именем с Microsoft Excel, Microsoft Excel перехватывает ошибку и по-прежнему задает **Error.Number** код Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="857fa-112">Note that if the error is generated in another object called by Microsoft Excel, Microsoft Excel intercepts the error and still sets **Error.Number** to the Microsoft Excel code.</span></span> <span data-ttu-id="857fa-113">Тем не менее другие **ошибки** объекта свойства (в том числе **источника**) будет сохранять значения как набор объектом, вызвавшей ошибку.</span><span class="sxs-lookup"><span data-stu-id="857fa-113">However, the other **Error** object properties (including **Source**) will retain the values as set by the object that generated the error.</span></span> <span data-ttu-id="857fa-114">Свойство **Source** всегда содержит имя объекта, вызвавшего ошибку.</span><span class="sxs-lookup"><span data-stu-id="857fa-114">The **Source** property always contains the name of the object that originally generated the error.</span></span>

<span data-ttu-id="857fa-115">На основе всей документацию ошибок, можно написать код, который будет обрабатывать ошибки соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="857fa-115">Based on all of the error documentation, you can write code that will handle the error appropriately.</span></span> <span data-ttu-id="857fa-116">Если обработчик ошибок не удается, можно использовать объект сведения **[об ошибке](error-object-dao.md)** для описания для пользователя, с помощью свойства **источника** и другие свойства **об ошибках** для предоставления пользователю информации о какой объект изначально, возникающие ошибки Ошибка, описание ошибки и т. д.</span><span class="sxs-lookup"><span data-stu-id="857fa-116">If your error handler fails, you can use the **[Error](error-object-dao.md)** object information to describe the error to your user, using the **Source** property and the other **Error** properties to give the user information about which object originally caused the error, the description of the error, and so forth.</span></span>


> [!NOTE]
> <P><span data-ttu-id="857fa-117">Конструкция <STRONG>On Error Resume Next</STRONG> может оказаться предпочтительнее <STRONG>On Error GoTo</STRONG> при работе с ошибки, возникающие во время доступа к другим объектам.</span><span class="sxs-lookup"><span data-stu-id="857fa-117">The <STRONG>On Error Resume Next</STRONG> construct may be preferable to <STRONG>On Error GoTo</STRONG> when dealing with errors generated during access to other objects.</span></span> <span data-ttu-id="857fa-118">Проверка свойства объекта <STRONG>ошибки</STRONG> после каждого взаимодействия с объектом устраняет неопределенность, о которых объект кода доступ к при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="857fa-118">Checking the <STRONG>Error</STRONG> object property after each interaction with an object removes ambiguity about which object your code was accessing when the error occurred.</span></span> <span data-ttu-id="857fa-119">Таким образом вам может быть том, какой объект поместил код ошибки в <STRONG>Error.Number</STRONG>, а также какой объект изначально создал ошибку (<STRONG>Error.Source</STRONG>).</span><span class="sxs-lookup"><span data-stu-id="857fa-119">Thus, you can be sure which object placed the error code in <STRONG>Error.Number</STRONG>, as well as which object originally generated the error (<STRONG>Error.Source</STRONG>).</span></span></P>



## <a name="example"></a><span data-ttu-id="857fa-120">Пример</span><span class="sxs-lookup"><span data-stu-id="857fa-120">Example</span></span>

<span data-ttu-id="857fa-121">В этом примере принудительно ошибку, его перехватывает и отображает свойства **Description**, **номер**, **источник**, **HelpContext**и **HelpFile** итоговый объект **Error** .</span><span class="sxs-lookup"><span data-stu-id="857fa-121">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

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
