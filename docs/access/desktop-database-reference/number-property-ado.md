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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707473"
---
# <a name="number-property-ado"></a><span data-ttu-id="c2c0e-102">Свойство Number (ADO)</span><span class="sxs-lookup"><span data-stu-id="c2c0e-102">Number property (ADO)</span></span>


<span data-ttu-id="c2c0e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2c0e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c2c0e-104">Указывает число, уникально идентифицирующий объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="c2c0e-104">Indicates the number that uniquely identifies an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="c2c0e-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2c0e-105">Return value</span></span>

<span data-ttu-id="c2c0e-106">Возвращает значение типа **Long** , могут соответствовать одному из константы [ErrorValueEnum](errorvalueenum.md) .</span><span class="sxs-lookup"><span data-stu-id="c2c0e-106">Returns a **Long** value that may correspond to one of the [ErrorValueEnum](errorvalueenum.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2c0e-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="c2c0e-107">Remarks</span></span>

<span data-ttu-id="c2c0e-108">Используйте свойство **номер** для определения, какая ошибка произошла.</span><span class="sxs-lookup"><span data-stu-id="c2c0e-108">Use the **Number** property to determine which error occurred.</span></span> <span data-ttu-id="c2c0e-109">Значение свойства — это уникальное число, соответствующее условия ошибки.</span><span class="sxs-lookup"><span data-stu-id="c2c0e-109">The value of the property is a unique number that corresponds to the error condition.</span></span>

<span data-ttu-id="c2c0e-110">Семейство [Errors](errors-collection-ado.md) возвращает значение HRESULT в шестнадцатеричном формате (например, 0x80004005) или длинное значение (например, 2147467259).</span><span class="sxs-lookup"><span data-stu-id="c2c0e-110">The [Errors](errors-collection-ado.md) collection returns an HRESULT in either hexadecimal format (for example, 0x80004005) or long value (for example, 2147467259).</span></span> <span data-ttu-id="c2c0e-111">Эти значения HRESULT может вызываться базовых компонентах, таких как OLE DB или даже OLE самого.</span><span class="sxs-lookup"><span data-stu-id="c2c0e-111">These HRESULTs can be raised by underlying components, such as OLE DB or even OLE itself.</span></span> <span data-ttu-id="c2c0e-112">Дополнительные сведения об этих номеров см из *Справочник программиста OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="c2c0e-112">For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

