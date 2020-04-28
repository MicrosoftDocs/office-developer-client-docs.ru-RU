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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288667"
---
# <a name="name-property-ado"></a><span data-ttu-id="1f0fa-102">Свойство Name (ADO)</span><span class="sxs-lookup"><span data-stu-id="1f0fa-102">Name property (ADO)</span></span>


<span data-ttu-id="1f0fa-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f0fa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f0fa-104">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="1f0fa-104">Indicates the name of an object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="1f0fa-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="1f0fa-105">Settings and return values</span></span>

<span data-ttu-id="1f0fa-106">Задает или возвращает **строковое** значение, указывающее имя объекта.</span><span class="sxs-lookup"><span data-stu-id="1f0fa-106">Sets or returns a **String** value that indicates the name of an object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f0fa-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="1f0fa-107">Remarks</span></span>

<span data-ttu-id="1f0fa-108">Используйте свойство **Name** для присвоения имени или извлечения имени **команды**, **Свойства**, **поля**или объекта **параметра** .</span><span class="sxs-lookup"><span data-stu-id="1f0fa-108">Use the **Name** property to assign a name to or retrieve the name of a **Command**, **Property**, **Field**, or **Parameter** object.</span></span>

<span data-ttu-id="1f0fa-109">Значение доступно для чтения и записи в объекте **Command** и доступно только для чтения для объекта **Property** .</span><span class="sxs-lookup"><span data-stu-id="1f0fa-109">The value is read/write on a **Command** object and read-only on a **Property** object.</span></span>

<span data-ttu-id="1f0fa-110">Для объекта **поля** **имя** обычно имеет значение "только для чтения".</span><span class="sxs-lookup"><span data-stu-id="1f0fa-110">For a **Field** object, **Name** is normally read-only.</span></span> <span data-ttu-id="1f0fa-111">Однако для новых объектов **field** , добавленных в коллекцию [Fields](fields-collection-ado.md) [записи](record-object-ado.md), **имя** доступно для чтения и записи только после того, как было указано свойство [value](value-property-ado.md) для **поля** , и поставщик данных успешно добавил новое **поле** , вызвав метод [Update](update-method-ado.md) коллекции **Fields** .</span><span class="sxs-lookup"><span data-stu-id="1f0fa-111">However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Name** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="1f0fa-112">Для объектов **Parameter** , еще не добавленных в коллекцию [Parameters](parameters-collection-ado.md) , свойство **Name** доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1f0fa-112">For **Parameter** objects not yet appended to the [Parameters](parameters-collection-ado.md) collection, the **Name** property is read/write.</span></span> <span data-ttu-id="1f0fa-113">Для добавленных объектов **Parameter** и всех других объектов свойство **Name** доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1f0fa-113">For appended **Parameter** objects and all other objects, the **Name** property is read-only.</span></span> <span data-ttu-id="1f0fa-114">Имена не обязательно должны быть уникальными в пределах коллекции.</span><span class="sxs-lookup"><span data-stu-id="1f0fa-114">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="1f0fa-115">Вы можете получить свойство **Name** объекта по порядковому номеру, после чего вы можете ссылаться на объект напрямую по имени.</span><span class="sxs-lookup"><span data-stu-id="1f0fa-115">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name.</span></span> <span data-ttu-id="1f0fa-116">Например, если Рстмаин. Properties (20). Name дает возможность обновления, поэтому вы можете ссылаться на это свойство в качестве результата обновления, поэтому вы можете ссылаться на это свойство как Рстмаин. Properties ("обновление").</span><span class="sxs-lookup"><span data-stu-id="1f0fa-116">For example, if rstMain.Properties(20).Name yields Updatability , you can subsequently refer to this property as yields Updatability , you can subsequently refer to this property as rstMain.Properties("Updatability") .</span></span>

