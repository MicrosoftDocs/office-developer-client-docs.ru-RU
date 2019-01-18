---
title: Коллекция Fields (ADO)
TOCTitle: Fields collection (ADO)
ms:assetid: 029aa738-8726-54a6-1813-b152813948bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248791(v=office.15)
ms:contentKeyID: 48542962
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a537756483361733c087d5dc1c6bba6e649d17d6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726262"
---
# <a name="fields-collection-ado"></a><span data-ttu-id="d663d-102">Коллекция Fields (ADO)</span><span class="sxs-lookup"><span data-stu-id="d663d-102">Fields collection (ADO)</span></span>


<span data-ttu-id="d663d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d663d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d663d-104">Содержит все объекты [поля](field-object-ado.md) объекта [набора записей](recordset-object-ado.md) или [записи](record-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d663d-104">Contains all the [Field](field-object-ado.md) objects of a [Recordset](recordset-object-ado.md) or [Record](record-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d663d-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="d663d-105">Remarks</span></span>

<span data-ttu-id="d663d-106">Объект **набора записей** имеет коллекции **полей** , состоящих из **поля** объектов.</span><span class="sxs-lookup"><span data-stu-id="d663d-106">A **Recordset** object has a **Fields** collection made up of **Field** objects.</span></span> <span data-ttu-id="d663d-107">Каждый объект **поля** соответствует столбца в **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="d663d-107">Each **Field** object corresponds to a column in the **Recordset**.</span></span> <span data-ttu-id="d663d-108">Можно заполнить коллекции **полей** перед открытием **набора записей** путем вызова метода [обновления](refresh-method-ado.md) в семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="d663d-108">You can populate the **Fields** collection before opening the **Recordset** by calling the [Refresh](refresh-method-ado.md) method on the collection.</span></span>

> [!NOTE]
> <span data-ttu-id="d663d-109">В разделе **поля** объекта более подробное описание того, как использовать объекты **поля** .</span><span class="sxs-lookup"><span data-stu-id="d663d-109">See the **Field** object topic for a more detailed explanation of how to use **Field** objects.</span></span>

<span data-ttu-id="d663d-110">Коллекция **полей** содержит метод [Append](append-method-ado.md) , который условно создает и добавляет объект **поля** в коллекцию и метод **Update** , который завершает добавлений или удалений.</span><span class="sxs-lookup"><span data-stu-id="d663d-110">The **Fields** collection has an [Append](append-method-ado.md) method, which provisionally creates and adds a **Field** object to the collection, and an **Update** method, which finalizes any additions or deletions.</span></span>

<span data-ttu-id="d663d-111">Объект **записи** имеет два особых полей, которые могут быть индексированы с [FieldEnum](fieldenum.md) константы.</span><span class="sxs-lookup"><span data-stu-id="d663d-111">A **Record** object has two special fields that can be indexed with [FieldEnum](fieldenum.md) constants.</span></span> <span data-ttu-id="d663d-112">Один константу обращается к поле, содержащее поток по умолчанию для **записи**и других операций доступа поле, содержащее строку абсолютный URL-адрес для **записи**.</span><span class="sxs-lookup"><span data-stu-id="d663d-112">One constant accesses a field containing the default stream for the **Record**, and the other accesses a field containing the absolute URL string for the **Record**.</span></span>

<span data-ttu-id="d663d-113">Определенных поставщиков (например, [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md)) могут заполнить коллекции **полей** с подмножеством доступные поля для **записи** или **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="d663d-113">Certain providers (for example, the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)) may populate the **Fields** collection with a subset of available fields for the **Record** or **Recordset**.</span></span> <span data-ttu-id="d663d-114">В остальных полях не добавляются в коллекцию до сначала по ссылке по имени или индексированные кода.</span><span class="sxs-lookup"><span data-stu-id="d663d-114">Other fields will not be added to the collection until they are first referenced by name or indexed by your code.</span></span>

<span data-ttu-id="d663d-115">При попытке сослаться на несуществующий поле по имени, новый объект **поля** будет добавлено в коллекцию **полей** с [состояние](status-property-ado-field.md) **adFieldPendingInsert**.</span><span class="sxs-lookup"><span data-stu-id="d663d-115">If you attempt to reference a nonexistent field by name, a new **Field** object will be appended to the **Fields** collection with a [Status](status-property-ado-field.md) of **adFieldPendingInsert**.</span></span> <span data-ttu-id="d663d-116">При вызове [Update](update-method-ado.md)ADO создаст новое поле из источника данных, если это разрешено ваш поставщик.</span><span class="sxs-lookup"><span data-stu-id="d663d-116">When you call [Update](update-method-ado.md), ADO will create a new field in your data source if allowed by your provider.</span></span>

