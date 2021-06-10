---
title: Коллекция полей (ADO)
TOCTitle: Fields collection (ADO)
ms:assetid: 029aa738-8726-54a6-1813-b152813948bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248791(v=office.15)
ms:contentKeyID: 48542962
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a537756483361733c087d5dc1c6bba6e649d17d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292575"
---
# <a name="fields-collection-ado"></a><span data-ttu-id="ec742-102">Коллекция полей (ADO)</span><span class="sxs-lookup"><span data-stu-id="ec742-102">Fields collection (ADO)</span></span>


<span data-ttu-id="ec742-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec742-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ec742-104">Содержит все [объекты Поля](field-object-ado.md) объекта [Recordset](recordset-object-ado.md) или [Record.](record-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="ec742-104">Contains all the [Field](field-object-ado.md) objects of a [Recordset](recordset-object-ado.md) or [Record](record-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec742-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="ec742-105">Remarks</span></span>

<span data-ttu-id="ec742-106">Объект **Recordset** имеет коллекцию **Полей,** которая состоит из **объектов Field.**</span><span class="sxs-lookup"><span data-stu-id="ec742-106">A **Recordset** object has a **Fields** collection made up of **Field** objects.</span></span> <span data-ttu-id="ec742-107">Каждый объект **Field** соответствует столбцу в **Наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="ec742-107">Each **Field** object corresponds to a column in the **Recordset**.</span></span> <span data-ttu-id="ec742-108">Вы можете заполнить коллекцию **Полей** перед открытием **Набор записей,** позвонив [методу Обновления](refresh-method-ado.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="ec742-108">You can populate the **Fields** collection before opening the **Recordset** by calling the [Refresh](refresh-method-ado.md) method on the collection.</span></span>

> [!NOTE]
> <span data-ttu-id="ec742-109">Дополнительные сведения об использовании объектов **Field** см. в разделе **Объект Field.**</span><span class="sxs-lookup"><span data-stu-id="ec742-109">See the **Field** object topic for a more detailed explanation of how to use **Field** objects.</span></span>

<span data-ttu-id="ec742-110">В **коллекции Fields** есть метод [Приложения,](append-method-ado.md) который предварительно создает и добавляет объект **Field** в коллекцию, а также метод **Update,** который завершает любые добавления или удаления.</span><span class="sxs-lookup"><span data-stu-id="ec742-110">The **Fields** collection has an [Append](append-method-ado.md) method, which provisionally creates and adds a **Field** object to the collection, and an **Update** method, which finalizes any additions or deletions.</span></span>

<span data-ttu-id="ec742-111">Объект **Record** имеет два специальных поля, которые можно индексировать с помощью [констант FieldEnum.](fieldenum.md)</span><span class="sxs-lookup"><span data-stu-id="ec742-111">A **Record** object has two special fields that can be indexed with [FieldEnum](fieldenum.md) constants.</span></span> <span data-ttu-id="ec742-112">Один постоянный доступ к поле, содержащее поток записи по **умолчанию,** а другой доступ к поле, содержащее абсолютную строку URL-адреса для **записи**.</span><span class="sxs-lookup"><span data-stu-id="ec742-112">One constant accesses a field containing the default stream for the **Record**, and the other accesses a field containing the absolute URL string for the **Record**.</span></span>

<span data-ttu-id="ec742-113">Некоторые поставщики (например, поставщик [microsoft OLE DB](microsoft-ole-db-provider-for-internet-publishing.md)для интернет-публикации) могут заполнить коллекцию **Fields** подмножество доступных полей для **Записи** или **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="ec742-113">Certain providers (for example, the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)) may populate the **Fields** collection with a subset of available fields for the **Record** or **Recordset**.</span></span> <span data-ttu-id="ec742-114">Другие поля не будут добавлены в коллекцию, пока они не будут впервые ссылаться по имени или индексироваться кодом.</span><span class="sxs-lookup"><span data-stu-id="ec742-114">Other fields will not be added to the collection until they are first referenced by name or indexed by your code.</span></span>

<span data-ttu-id="ec742-115">Если вы попытается ссылаться на несущестующие поля по имени, новый объект [](status-property-ado-field.md) **Field** будет пристроен к коллекции **Fields** со статусом **adFieldPendingInsert.**</span><span class="sxs-lookup"><span data-stu-id="ec742-115">If you attempt to reference a nonexistent field by name, a new **Field** object will be appended to the **Fields** collection with a [Status](status-property-ado-field.md) of **adFieldPendingInsert**.</span></span> <span data-ttu-id="ec742-116">При [вызове Update](update-method-ado.md)ADO создаст новое поле в источнике данных, если это разрешено поставщиком.</span><span class="sxs-lookup"><span data-stu-id="ec742-116">When you call [Update](update-method-ado.md), ADO will create a new field in your data source if allowed by your provider.</span></span>

