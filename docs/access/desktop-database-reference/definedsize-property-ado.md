---
title: Свойство DefinedSize (ADO)
TOCTitle: DefinedSize property (ADO)
ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15)
ms:contentKeyID: 48546257
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 121e81734fc5ecc0a761dae53942f1cbed98df2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294136"
---
# <a name="definedsize-property-ado"></a><span data-ttu-id="a6c6f-102">Свойство DefinedSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="a6c6f-102">DefinedSize property (ADO)</span></span>


<span data-ttu-id="a6c6f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a6c6f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a6c6f-104">Указывает емкость данных объекта [Field.](field-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="a6c6f-104">Indicates the data capacity of a [Field](field-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="a6c6f-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a6c6f-105">Return value</span></span>

<span data-ttu-id="a6c6f-106">Возвращает **длинное значение,** отражающие определенный размер поля в количестве ветвей.</span><span class="sxs-lookup"><span data-stu-id="a6c6f-106">Returns a **Long** value that reflects the defined size of a field as a number of bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6c6f-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="a6c6f-107">Remarks</span></span>

<span data-ttu-id="a6c6f-108">Используйте свойство **DefinedSize** для определения емкости данных объекта **Field.**</span><span class="sxs-lookup"><span data-stu-id="a6c6f-108">Use the **DefinedSize** property to determine the data capacity of a **Field** object.</span></span>

<span data-ttu-id="a6c6f-109">Свойства **DefinedSize** и [ActualSize](actualsize-property-ado.md) отличаются.</span><span class="sxs-lookup"><span data-stu-id="a6c6f-109">The **DefinedSize** and [ActualSize](actualsize-property-ado.md) properties are different.</span></span> <span data-ttu-id="a6c6f-110">Например, рассмотрим объект **Field** с объявленным типом **adVarChar** и значением свойства **DefinedSize** 50, содержащим один символ.</span><span class="sxs-lookup"><span data-stu-id="a6c6f-110">For example, consider a **Field** object with a declared type of **adVarChar** and a **DefinedSize** property value of 50, containing a single character.</span></span> <span data-ttu-id="a6c6f-111">Возвращаемая величина свойства **ActualSize** — это длина в ветвях одного символа.</span><span class="sxs-lookup"><span data-stu-id="a6c6f-111">The **ActualSize** property value it returns is the length in bytes of the single character.</span></span>

