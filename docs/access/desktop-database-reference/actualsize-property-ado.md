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
# <a name="actualsize-property-ado"></a><span data-ttu-id="3565e-102">Свойство ActualSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="3565e-102">ActualSize property (ADO)</span></span>

<span data-ttu-id="3565e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3565e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3565e-104">Указывает фактическую длину значения поля.</span><span class="sxs-lookup"><span data-stu-id="3565e-104">Indicates the actual length of a field's value.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3565e-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3565e-105">Settings and return values</span></span>

<span data-ttu-id="3565e-106">Возвращает значение **типа Long** .</span><span class="sxs-lookup"><span data-stu-id="3565e-106">Returns a **Long** value.</span></span> <span data-ttu-id="3565e-107">Некоторые поставщики могут разрешить этому свойству зарезервировать пространство для данных BLOB, в этом случае значение по умолчанию равно 0.</span><span class="sxs-lookup"><span data-stu-id="3565e-107">Some providers may allow this property to be set to reserve space for BLOB data, in which case the default value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="3565e-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="3565e-108">Remarks</span></span>

<span data-ttu-id="3565e-109">Используйте свойство **ActualSize** , чтобы возвратить фактическую длину значения объекта [field](field-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="3565e-109">Use the **ActualSize** property to return the actual length of a [Field](field-object-ado.md) object's value.</span></span> <span data-ttu-id="3565e-110">Для всех полей свойство **ActualSize** доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3565e-110">For all fields, the **ActualSize** property is read-only.</span></span> <span data-ttu-id="3565e-111">Если ADO не удается определить длину значения объекта **field** , свойство **ActualSize** возвращает **адункновн**.</span><span class="sxs-lookup"><span data-stu-id="3565e-111">If ADO cannot determine the length of the **Field** object's value, the **ActualSize** property returns **adUnknown**.</span></span>

<span data-ttu-id="3565e-112">Свойства **ActualSize** и [DefinedSize](definedsize-property-ado.md) отличаются.</span><span class="sxs-lookup"><span data-stu-id="3565e-112">The **ActualSize** and [DefinedSize](definedsize-property-ado.md) properties are different.</span></span> <span data-ttu-id="3565e-113">Объект **field** с объявляемым типом **адварчар** и максимальной длиной 50 символов возвращает значение свойства **DefinedSize** 50, но возвращаемое значение свойства **ActualSize** — это длина данных, хранящихся в поле для Текущая запись.</span><span class="sxs-lookup"><span data-stu-id="3565e-113">A **Field** object with a declared type of **adVarChar** and a maximum length of 50 characters returns a **DefinedSize** property value of 50, but the **ActualSize** property value it returns is the length of the data stored in the field for the current record.</span></span> <span data-ttu-id="3565e-114">**Поля** с **DefinedSize** , превышающие 255 байт, считаются столбцами переменной длины.</span><span class="sxs-lookup"><span data-stu-id="3565e-114">**Fields** with a **DefinedSize** greater than 255 bytes are treated as variable length columns.</span></span>

