---
title: DefinedSize Property (ADO)
TOCTitle: DefinedSize Property (ADO)
ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15)
ms:contentKeyID: 48546257
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a8ffd8bb24abcab737ebc4bb23a0af717c02d486
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480336"
---
# <a name="definedsize-property-ado"></a><span data-ttu-id="963fa-102">DefinedSize Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="963fa-102">DefinedSize Property (ADO)</span></span>


<span data-ttu-id="963fa-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="963fa-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="963fa-104">Указывает объем данных объекта [поля](field-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="963fa-104">Indicates the data capacity of a [Field](field-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="963fa-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="963fa-105">Return Value</span></span>

<span data-ttu-id="963fa-106">Возвращает значение типа **Long** , отражает определенный размер поля в байтах.</span><span class="sxs-lookup"><span data-stu-id="963fa-106">Returns a **Long** value that reflects the defined size of a field as a number of bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="963fa-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="963fa-107">Remarks</span></span>

<span data-ttu-id="963fa-108">Свойство **DefinedSize** используется для определения емкости данных объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="963fa-108">Use the **DefinedSize** property to determine the data capacity of a **Field** object.</span></span>

<span data-ttu-id="963fa-109">Свойства **DefinedSize** и [ActualSize](actualsize-property-ado.md) не совпадают.</span><span class="sxs-lookup"><span data-stu-id="963fa-109">The **DefinedSize** and [ActualSize](actualsize-property-ado.md) properties are different.</span></span> <span data-ttu-id="963fa-110">Например рассмотрим объект **Field** с типом объявленные **adVarChar** и значение свойства **DefinedSize** 50, содержащий один символ.</span><span class="sxs-lookup"><span data-stu-id="963fa-110">For example, consider a **Field** object with a declared type of **adVarChar** and a **DefinedSize** property value of 50, containing a single character.</span></span> <span data-ttu-id="963fa-111">**ActualSize** свойство возвращает значение длины в байтах один символ.</span><span class="sxs-lookup"><span data-stu-id="963fa-111">The **ActualSize** property value it returns is the length in bytes of the single character.</span></span>

