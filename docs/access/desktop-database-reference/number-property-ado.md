---
title: Свойство Number (ADO)
TOCTitle: Number property (ADO)
ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15)
ms:contentKeyID: 48547243
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5eb46d6fbeb677e6d0fe73223d74ae2ea42d368
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288576"
---
# <a name="number-property-ado"></a><span data-ttu-id="b5325-102">Свойство Number (ADO)</span><span class="sxs-lookup"><span data-stu-id="b5325-102">Number property (ADO)</span></span>


<span data-ttu-id="b5325-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b5325-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b5325-104">Указывает номер, который однозначно идентифицирует объект [Error.](error-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b5325-104">Indicates the number that uniquely identifies an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="b5325-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5325-105">Return value</span></span>

<span data-ttu-id="b5325-106">Возвращает значение **Long,** которое может соответствовать одной из констант [ErrorValueEnum.](errorvalueenum.md)</span><span class="sxs-lookup"><span data-stu-id="b5325-106">Returns a **Long** value that may correspond to one of the [ErrorValueEnum](errorvalueenum.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5325-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="b5325-107">Remarks</span></span>

<span data-ttu-id="b5325-108">Чтобы **определить,** какая ошибка произошла, используйте свойство Number.</span><span class="sxs-lookup"><span data-stu-id="b5325-108">Use the **Number** property to determine which error occurred.</span></span> <span data-ttu-id="b5325-109">Значение свойства — уникальный номер, соответствующий условию ошибки.</span><span class="sxs-lookup"><span data-stu-id="b5325-109">The value of the property is a unique number that corresponds to the error condition.</span></span>

<span data-ttu-id="b5325-110">Коллекция [Ошибок](errors-collection-ado.md) возвращает HRESULT в шестидесятиградном формате (например, 0x80004005) или длинном значении (например, 2147467259).</span><span class="sxs-lookup"><span data-stu-id="b5325-110">The [Errors](errors-collection-ado.md) collection returns an HRESULT in either hexadecimal format (for example, 0x80004005) or long value (for example, 2147467259).</span></span> <span data-ttu-id="b5325-111">Эти HRESULTs могут быть подняты с помощью основных компонентов, таких как OLE DB или даже сам OLE.</span><span class="sxs-lookup"><span data-stu-id="b5325-111">These HRESULTs can be raised by underlying components, such as OLE DB or even OLE itself.</span></span> <span data-ttu-id="b5325-112">Дополнительные сведения об этих номерах см. в главе 16 справочника программиста *OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="b5325-112">For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

