---
title: Name Property (ADO)
TOCTitle: Name Property (ADO)
ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15)
ms:contentKeyID: 48544683
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 132d00af1aecf7ec1ae8fbdb7855a10dd99c7f4f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482588"
---
# <a name="name-property-ado"></a><span data-ttu-id="91a7a-102">Name Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="91a7a-102">Name Property (ADO)</span></span>


<span data-ttu-id="91a7a-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="91a7a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="91a7a-104">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="91a7a-104">Indicates the name of an object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="91a7a-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="91a7a-105">Settings and Return Values</span></span>

<span data-ttu-id="91a7a-106">Задает или возвращает **строковое** значение, указывающее имя объекта.</span><span class="sxs-lookup"><span data-stu-id="91a7a-106">Sets or returns a **String** value that indicates the name of an object.</span></span>

## <a name="remarks"></a><span data-ttu-id="91a7a-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="91a7a-107">Remarks</span></span>

<span data-ttu-id="91a7a-108">Используйте свойство **Name** назначение имени или получить имя объекта **команды**, **Свойства**, **поля**или **параметра** .</span><span class="sxs-lookup"><span data-stu-id="91a7a-108">Use the **Name** property to assign a name to or retrieve the name of a **Command**, **Property**, **Field**, or **Parameter** object.</span></span>

<span data-ttu-id="91a7a-109">Значение является чтение и запись в объект **команды** и только для чтения **свойство** объекта.</span><span class="sxs-lookup"><span data-stu-id="91a7a-109">The value is read/write on a **Command** object and read-only on a **Property** object.</span></span>

<span data-ttu-id="91a7a-110">Для объекта **поля** **имя** обычно доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="91a7a-110">For a **Field** object, **Name** is normally read-only.</span></span> <span data-ttu-id="91a7a-111">Тем не менее для новых объектов **полей** , к коллекции [полей](fields-collection-ado.md) [записи](record-object-ado.md), **имя** — чтение и запись только после того, как указано [значение](value-property-ado.md) свойства для **поля** и имеет поставщика данных успешно добавлено новое **поле** , вызвав метод [Update](update-method-ado.md) коллекции **полей** .</span><span class="sxs-lookup"><span data-stu-id="91a7a-111">However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Name** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="91a7a-112">Для **параметра** объектов еще не добавляются в коллекцию [параметров](parameters-collection-ado.md) свойство **Name** — чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="91a7a-112">For **Parameter** objects not yet appended to the [Parameters](parameters-collection-ado.md) collection, the **Name** property is read/write.</span></span> <span data-ttu-id="91a7a-113">Для присоединенных объекты **параметров** и другие объекты свойства **Name** — только для чтения.</span><span class="sxs-lookup"><span data-stu-id="91a7a-113">For appended **Parameter** objects and all other objects, the **Name** property is read-only.</span></span> <span data-ttu-id="91a7a-114">Имена не обязательно должно быть уникальным в семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="91a7a-114">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="91a7a-115">Свойство **Name** объекта можно извлечь с помощью порядковый номер ссылки, после чего можно обратиться к объекту непосредственно по имени.</span><span class="sxs-lookup"><span data-stu-id="91a7a-115">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name.</span></span> <span data-ttu-id="91a7a-116">Например если rstMain.Properties(20). Имя дает возможность обновления, впоследствии можно ссылаться на это свойство как дает возможность обновления, впоследствии можно ссылаться на это свойство как rstMain.Properties("Updatability").</span><span class="sxs-lookup"><span data-stu-id="91a7a-116">For example, if rstMain.Properties(20).Name yields Updatability , you can subsequently refer to this property as yields Updatability , you can subsequently refer to this property as rstMain.Properties("Updatability") .</span></span>

