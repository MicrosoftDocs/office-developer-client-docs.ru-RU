---
title: Свойство Name (ADO)
TOCTitle: Name property (ADO)
ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15)
ms:contentKeyID: 48544683
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f6fbfbd7008919cc4d784a4d0468d8471d102708
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721549"
---
# <a name="name-property-ado"></a><span data-ttu-id="87305-102">Свойство Name (ADO)</span><span class="sxs-lookup"><span data-stu-id="87305-102">Name property (ADO)</span></span>


<span data-ttu-id="87305-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="87305-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="87305-104">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="87305-104">Indicates the name of an object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="87305-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="87305-105">Settings and return values</span></span>

<span data-ttu-id="87305-106">Задает или возвращает **строковое** значение, указывающее имя объекта.</span><span class="sxs-lookup"><span data-stu-id="87305-106">Sets or returns a **String** value that indicates the name of an object.</span></span>

## <a name="remarks"></a><span data-ttu-id="87305-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="87305-107">Remarks</span></span>

<span data-ttu-id="87305-108">Используйте свойство **Name** назначение имени или получить имя объекта **команды**, **Свойства**, **поля**или **параметра** .</span><span class="sxs-lookup"><span data-stu-id="87305-108">Use the **Name** property to assign a name to or retrieve the name of a **Command**, **Property**, **Field**, or **Parameter** object.</span></span>

<span data-ttu-id="87305-109">Значение является чтение и запись в объект **команды** и только для чтения **свойство** объекта.</span><span class="sxs-lookup"><span data-stu-id="87305-109">The value is read/write on a **Command** object and read-only on a **Property** object.</span></span>

<span data-ttu-id="87305-110">Для объекта **поля** **имя** обычно доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="87305-110">For a **Field** object, **Name** is normally read-only.</span></span> <span data-ttu-id="87305-111">Тем не менее для новых объектов **полей** , к коллекции [полей](fields-collection-ado.md) [записи](record-object-ado.md), **имя** — чтение и запись только после того, как указано [значение](value-property-ado.md) свойства для **поля** и имеет поставщика данных успешно добавлено новое **поле** , вызвав метод [Update](update-method-ado.md) коллекции **полей** .</span><span class="sxs-lookup"><span data-stu-id="87305-111">However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Name** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="87305-112">Для **параметра** объектов еще не добавляются в коллекцию [параметров](parameters-collection-ado.md) свойство **Name** — чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="87305-112">For **Parameter** objects not yet appended to the [Parameters](parameters-collection-ado.md) collection, the **Name** property is read/write.</span></span> <span data-ttu-id="87305-113">Для присоединенных объекты **параметров** и другие объекты свойства **Name** — только для чтения.</span><span class="sxs-lookup"><span data-stu-id="87305-113">For appended **Parameter** objects and all other objects, the **Name** property is read-only.</span></span> <span data-ttu-id="87305-114">Имена не обязательно должно быть уникальным в семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="87305-114">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="87305-115">Свойство **Name** объекта можно извлечь с помощью порядковый номер ссылки, после чего можно обратиться к объекту непосредственно по имени.</span><span class="sxs-lookup"><span data-stu-id="87305-115">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name.</span></span> <span data-ttu-id="87305-116">Например если rstMain.Properties(20). Имя дает возможность обновления, впоследствии можно ссылаться на это свойство как дает возможность обновления, впоследствии можно ссылаться на это свойство как rstMain.Properties("Updatability").</span><span class="sxs-lookup"><span data-stu-id="87305-116">For example, if rstMain.Properties(20).Name yields Updatability , you can subsequently refer to this property as yields Updatability , you can subsequently refer to this property as rstMain.Properties("Updatability") .</span></span>

