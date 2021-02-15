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
# <a name="actualsize-property-ado"></a><span data-ttu-id="45151-102">Свойство ActualSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="45151-102">ActualSize property (ADO)</span></span>

<span data-ttu-id="45151-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="45151-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="45151-104">Указывает фактическую длину значения поля.</span><span class="sxs-lookup"><span data-stu-id="45151-104">Indicates the actual length of a field's value.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="45151-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="45151-105">Settings and return values</span></span>

<span data-ttu-id="45151-106">Возвращает **длинное** значение.</span><span class="sxs-lookup"><span data-stu-id="45151-106">Returns a **Long** value.</span></span> <span data-ttu-id="45151-107">Некоторые поставщики могут разрешить этому свойству резервировать место для данных BLOB, в этом случае значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="45151-107">Some providers may allow this property to be set to reserve space for BLOB data, in which case the default value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="45151-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="45151-108">Remarks</span></span>

<span data-ttu-id="45151-109">Используйте свойство **ActualSize** для возврата фактической длины значения объекта [Field.](field-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="45151-109">Use the **ActualSize** property to return the actual length of a [Field](field-object-ado.md) object's value.</span></span> <span data-ttu-id="45151-110">Для всех полей свойство **ActualSize** имеет только чтение.</span><span class="sxs-lookup"><span data-stu-id="45151-110">For all fields, the **ActualSize** property is read-only.</span></span> <span data-ttu-id="45151-111">Если ADO не удается определить длину значения **объекта Field,** свойство **ActualSize** возвращает **adUnknown**.</span><span class="sxs-lookup"><span data-stu-id="45151-111">If ADO cannot determine the length of the **Field** object's value, the **ActualSize** property returns **adUnknown**.</span></span>

<span data-ttu-id="45151-112">Свойства **ActualSize** [и DefinedSize](definedsize-property-ado.md) отличаются.</span><span class="sxs-lookup"><span data-stu-id="45151-112">The **ActualSize** and [DefinedSize](definedsize-property-ado.md) properties are different.</span></span> <span data-ttu-id="45151-113">Объект **Field** с объявленным типом **adVarChar** и длиной не более 50 символов возвращает значение свойства **DefinedSize** 50, но возвращаемая величина свойства **ActualSize** является длиной данных, хранимых в поле для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="45151-113">A **Field** object with a declared type of **adVarChar** and a maximum length of 50 characters returns a **DefinedSize** property value of 50, but the **ActualSize** property value it returns is the length of the data stored in the field for the current record.</span></span> <span data-ttu-id="45151-114">**Поля** с **значением DefinedSize** больше 255байт обрабатываются как столбцы переменной длины.</span><span class="sxs-lookup"><span data-stu-id="45151-114">**Fields** with a **DefinedSize** greater than 255 bytes are treated as variable length columns.</span></span>

