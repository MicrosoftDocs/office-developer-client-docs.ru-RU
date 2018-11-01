---
title: Свойство ActualSize (ADO)
TOCTitle: ActualSize property (ADO)
ms:assetid: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15)
ms:contentKeyID: 48542949
ms.date: 10/16/2018
mtps_version: v=office.15
ms.openlocfilehash: 627f4fe93340c69b62f81c1b10ebf231938eea89
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873187"
---
# <a name="actualsize-property-ado"></a><span data-ttu-id="88f30-102">Свойство ActualSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="88f30-102">ActualSize property (ADO)</span></span>

<span data-ttu-id="88f30-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="88f30-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="88f30-104">Фактическая длина значения поля.</span><span class="sxs-lookup"><span data-stu-id="88f30-104">Indicates the actual length of a field's value.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="88f30-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="88f30-105">Settings and return values</span></span>

<span data-ttu-id="88f30-106">Возвращает значение типа **Long** .</span><span class="sxs-lookup"><span data-stu-id="88f30-106">Returns a **Long** value.</span></span> <span data-ttu-id="88f30-107">Некоторые поставщики могут разрешить это свойство должно быть задано для резервирования пространства для данных больших двоичных ОБЪЕКТОВ, в котором case значение по умолчанию равно 0.</span><span class="sxs-lookup"><span data-stu-id="88f30-107">Some providers may allow this property to be set to reserve space for BLOB data, in which case the default value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="88f30-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="88f30-108">Remarks</span></span>

<span data-ttu-id="88f30-109">Свойство **ActualSize** возвращает фактический длины значения объекта [поля](field-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="88f30-109">Use the **ActualSize** property to return the actual length of a [Field](field-object-ado.md) object's value.</span></span> <span data-ttu-id="88f30-110">Для всех полей **ActualSize** свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="88f30-110">For all fields, the **ActualSize** property is read-only.</span></span> <span data-ttu-id="88f30-111">Если ADO не может быть определен значение **поля** объекта, свойство **ActualSize** возвращает **adUnknown**.</span><span class="sxs-lookup"><span data-stu-id="88f30-111">If ADO cannot determine the length of the **Field** object's value, the **ActualSize** property returns **adUnknown**.</span></span>

<span data-ttu-id="88f30-112">Свойства **ActualSize** и [DefinedSize](definedsize-property-ado.md) не совпадают.</span><span class="sxs-lookup"><span data-stu-id="88f30-112">The **ActualSize** and [DefinedSize](definedsize-property-ado.md) properties are different.</span></span> <span data-ttu-id="88f30-113">Объект **Field** с типом объявленные **adVarChar** и максимальную длину 50 символов возвращает значение свойства **DefinedSize** 50, но она возвращает значение свойства **ActualSize** — это длина данных, сохраненных в процессе работы Текущая запись.</span><span class="sxs-lookup"><span data-stu-id="88f30-113">A **Field** object with a declared type of **adVarChar** and a maximum length of 50 characters returns a **DefinedSize** property value of 50, but the **ActualSize** property value it returns is the length of the data stored in the field for the current record.</span></span> <span data-ttu-id="88f30-114">**Поля** с **DefinedSize** быстрее, чем 255 байт обрабатывается как столбцы переменной длины.</span><span class="sxs-lookup"><span data-stu-id="88f30-114">**Fields** with a **DefinedSize** greater than 255 bytes are treated as variable length columns.</span></span>

