---
title: Свойство DefinedSize (ADO)
TOCTitle: DefinedSize property (ADO)
ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15)
ms:contentKeyID: 48546257
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0a0e67cfdbe60ebf2c49cb3e726311d2fa61bd3e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868856"
---
# <a name="definedsize-property-ado"></a><span data-ttu-id="5f783-102">Свойство DefinedSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="5f783-102">DefinedSize property (ADO)</span></span>


<span data-ttu-id="5f783-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5f783-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5f783-104">Указывает объем данных объекта [поля](field-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="5f783-104">Indicates the data capacity of a [Field](field-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f783-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f783-105">Return value</span></span>

<span data-ttu-id="5f783-106">Возвращает значение типа **Long** , отражает определенный размер поля в байтах.</span><span class="sxs-lookup"><span data-stu-id="5f783-106">Returns a **Long** value that reflects the defined size of a field as a number of bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f783-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="5f783-107">Remarks</span></span>

<span data-ttu-id="5f783-108">Свойство **DefinedSize** используется для определения емкости данных объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="5f783-108">Use the **DefinedSize** property to determine the data capacity of a **Field** object.</span></span>

<span data-ttu-id="5f783-109">Свойства **DefinedSize** и [ActualSize](actualsize-property-ado.md) не совпадают.</span><span class="sxs-lookup"><span data-stu-id="5f783-109">The **DefinedSize** and [ActualSize](actualsize-property-ado.md) properties are different.</span></span> <span data-ttu-id="5f783-110">Например рассмотрим объект **Field** с типом объявленные **adVarChar** и значение свойства **DefinedSize** 50, содержащий один символ.</span><span class="sxs-lookup"><span data-stu-id="5f783-110">For example, consider a **Field** object with a declared type of **adVarChar** and a **DefinedSize** property value of 50, containing a single character.</span></span> <span data-ttu-id="5f783-111">**ActualSize** свойство возвращает значение длины в байтах один символ.</span><span class="sxs-lookup"><span data-stu-id="5f783-111">The **ActualSize** property value it returns is the length in bytes of the single character.</span></span>

