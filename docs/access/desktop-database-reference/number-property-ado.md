---
title: Свойство Number (ADO)
TOCTitle: Number property (ADO)
ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15)
ms:contentKeyID: 48547243
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 72afba54062a3f103fe75939502c9f52eef4c44d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887200"
---
# <a name="number-property-ado"></a><span data-ttu-id="3026d-102">Свойство Number (ADO)</span><span class="sxs-lookup"><span data-stu-id="3026d-102">Number property (ADO)</span></span>


<span data-ttu-id="3026d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3026d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3026d-104">Указывает число, уникально идентифицирующий объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="3026d-104">Indicates the number that uniquely identifies an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="3026d-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3026d-105">Return value</span></span>

<span data-ttu-id="3026d-106">Возвращает значение типа **Long** , могут соответствовать одному из константы [ErrorValueEnum](errorvalueenum.md) .</span><span class="sxs-lookup"><span data-stu-id="3026d-106">Returns a **Long** value that may correspond to one of the [ErrorValueEnum](errorvalueenum.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="3026d-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="3026d-107">Remarks</span></span>

<span data-ttu-id="3026d-108">Используйте свойство **номер** для определения, какая ошибка произошла.</span><span class="sxs-lookup"><span data-stu-id="3026d-108">Use the **Number** property to determine which error occurred.</span></span> <span data-ttu-id="3026d-109">Значение свойства — это уникальное число, соответствующее условия ошибки.</span><span class="sxs-lookup"><span data-stu-id="3026d-109">The value of the property is a unique number that corresponds to the error condition.</span></span>

<span data-ttu-id="3026d-110">Семейство [Errors](errors-collection-ado.md) возвращает значение HRESULT в шестнадцатеричном формате (например, 0x80004005) или длинное значение (например, 2147467259).</span><span class="sxs-lookup"><span data-stu-id="3026d-110">The [Errors](errors-collection-ado.md) collection returns an HRESULT in either hexadecimal format (for example, 0x80004005) or long value (for example, 2147467259).</span></span> <span data-ttu-id="3026d-111">Эти значения HRESULT может вызываться базовых компонентах, таких как OLE DB или даже OLE самого.</span><span class="sxs-lookup"><span data-stu-id="3026d-111">These HRESULTs can be raised by underlying components, such as OLE DB or even OLE itself.</span></span> <span data-ttu-id="3026d-112">Дополнительные сведения об этих номеров см из *Справочник программиста OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="3026d-112">For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

