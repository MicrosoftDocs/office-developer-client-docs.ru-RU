---
title: Свойство ActualSize (ADO)
TOCTitle: ActualSize property (ADO)
ms:assetid: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15)
ms:contentKeyID: 48542949
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c13cb41299ddaf786e6412e43a50b1414ad818b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280434"
---
# <a name="actualsize-property-ado"></a><span data-ttu-id="f0201-102">Свойство ActualSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="f0201-102">ActualSize property (ADO)</span></span>

<span data-ttu-id="f0201-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0201-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f0201-104">Указывает фактическую длину значения поля.</span><span class="sxs-lookup"><span data-stu-id="f0201-104">Indicates the actual length of a field's value.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="f0201-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="f0201-105">Settings and return values</span></span>

<span data-ttu-id="f0201-106">Возвращает значение **Long.**</span><span class="sxs-lookup"><span data-stu-id="f0201-106">Returns a **Long** value.</span></span> <span data-ttu-id="f0201-107">Некоторые поставщики могут разрешить этому свойству зарезервировать пространство для данных BLOB, в этом случае значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="f0201-107">Some providers may allow this property to be set to reserve space for BLOB data, in which case the default value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0201-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="f0201-108">Remarks</span></span>

<span data-ttu-id="f0201-109">Используйте **свойство ActualSize,** чтобы вернуть фактическую длину значения [объекта Field.](field-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="f0201-109">Use the **ActualSize** property to return the actual length of a [Field](field-object-ado.md) object's value.</span></span> <span data-ttu-id="f0201-110">Для всех полей свойство **ActualSize** является только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f0201-110">For all fields, the **ActualSize** property is read-only.</span></span> <span data-ttu-id="f0201-111">Если ADO не может определить длину значения **объекта Field,** свойство **ActualSize** возвращает **adUnknown.**</span><span class="sxs-lookup"><span data-stu-id="f0201-111">If ADO cannot determine the length of the **Field** object's value, the **ActualSize** property returns **adUnknown**.</span></span>

<span data-ttu-id="f0201-112">Свойства **ActualSize** и [DefinedSize](definedsize-property-ado.md) отличаются.</span><span class="sxs-lookup"><span data-stu-id="f0201-112">The **ActualSize** and [DefinedSize](definedsize-property-ado.md) properties are different.</span></span> <span data-ttu-id="f0201-113">Объект **Field** с объявленным типом **adVarChar** и максимальной длиной 50 символов возвращает значение **Свойства DefinedSize** в 50, но возвращаемая значения **ActualSize** — это длина данных, хранимых в поле для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="f0201-113">A **Field** object with a declared type of **adVarChar** and a maximum length of 50 characters returns a **DefinedSize** property value of 50, but the **ActualSize** property value it returns is the length of the data stored in the field for the current record.</span></span> <span data-ttu-id="f0201-114">**Поля** с **значением DefinedSize** более 255 bytes рассматриваются как столбцы переменной длины.</span><span class="sxs-lookup"><span data-stu-id="f0201-114">**Fields** with a **DefinedSize** greater than 255 bytes are treated as variable length columns.</span></span>

