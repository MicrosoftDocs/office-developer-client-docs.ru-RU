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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292575"
---
# <a name="fields-collection-ado"></a><span data-ttu-id="34a50-102">Коллекция Fields (ADO)</span><span class="sxs-lookup"><span data-stu-id="34a50-102">Fields collection (ADO)</span></span>


<span data-ttu-id="34a50-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="34a50-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="34a50-104">Содержит все объекты [field](field-object-ado.md) объекта [Recordset](recordset-object-ado.md) или [записи](record-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="34a50-104">Contains all the [Field](field-object-ado.md) objects of a [Recordset](recordset-object-ado.md) or [Record](record-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="34a50-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="34a50-105">Remarks</span></span>

<span data-ttu-id="34a50-106">Объект **Recordset** содержит коллекцию **Fields** , состоящего из объектов **field** .</span><span class="sxs-lookup"><span data-stu-id="34a50-106">A **Recordset** object has a **Fields** collection made up of **Field** objects.</span></span> <span data-ttu-id="34a50-107">Каждый объект **field** соответствует столбцу в наборе **записей**.</span><span class="sxs-lookup"><span data-stu-id="34a50-107">Each **Field** object corresponds to a column in the **Recordset**.</span></span> <span data-ttu-id="34a50-108">Вы можете заполнить коллекцию **Fields** перед открытием **набора записей** , вызвав метод [Refresh](refresh-method-ado.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="34a50-108">You can populate the **Fields** collection before opening the **Recordset** by calling the [Refresh](refresh-method-ado.md) method on the collection.</span></span>

> [!NOTE]
> <span data-ttu-id="34a50-109">В разделе объект **field** описывается более подробное описание использования объектов **полей** .</span><span class="sxs-lookup"><span data-stu-id="34a50-109">See the **Field** object topic for a more detailed explanation of how to use **Field** objects.</span></span>

<span data-ttu-id="34a50-110">Коллекция **Fields** содержит метод [append](append-method-ado.md) , который подготавливает создание и добавление объекта **field** в коллекцию, и метод **Update** , который завершает все добавления и удаления.</span><span class="sxs-lookup"><span data-stu-id="34a50-110">The **Fields** collection has an [Append](append-method-ado.md) method, which provisionally creates and adds a **Field** object to the collection, and an **Update** method, which finalizes any additions or deletions.</span></span>

<span data-ttu-id="34a50-111">Объект **Record** содержит два специальных поля, которые можно индексировать с помощью констант [фиелденум](fieldenum.md) .</span><span class="sxs-lookup"><span data-stu-id="34a50-111">A **Record** object has two special fields that can be indexed with [FieldEnum](fieldenum.md) constants.</span></span> <span data-ttu-id="34a50-112">Одна константа получает доступ к полю, содержащему поток по умолчанию для **записи**, а другой обращается к полю, содержащему строку с АБСОЛЮТНЫМ URL-адресом для **записи**.</span><span class="sxs-lookup"><span data-stu-id="34a50-112">One constant accesses a field containing the default stream for the **Record**, and the other accesses a field containing the absolute URL string for the **Record**.</span></span>

<span data-ttu-id="34a50-113">Некоторые поставщики (например, [поставщик Microsoft OLE DB для публикации в Интернете](microsoft-ole-db-provider-for-internet-publishing.md)) могут заполнить коллекцию Fields \*\*\*\* подмножеством доступных полей для **записи** или **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="34a50-113">Certain providers (for example, the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)) may populate the **Fields** collection with a subset of available fields for the **Record** or **Recordset**.</span></span> <span data-ttu-id="34a50-114">Другие поля не добавляются в коллекцию до тех пор, пока они не будут первыми ссылаться на них по имени или индексировать код.</span><span class="sxs-lookup"><span data-stu-id="34a50-114">Other fields will not be added to the collection until they are first referenced by name or indexed by your code.</span></span>

<span data-ttu-id="34a50-115">При попытке ссылки на несуществующее поле по имени новый объект **field** будет добавлен в коллекцию **Fields** со [статусом](status-property-ado-field.md) **адфиелдпендингинсерт**.</span><span class="sxs-lookup"><span data-stu-id="34a50-115">If you attempt to reference a nonexistent field by name, a new **Field** object will be appended to the **Fields** collection with a [Status](status-property-ado-field.md) of **adFieldPendingInsert**.</span></span> <span data-ttu-id="34a50-116">Когда вы вызываете [Update](update-method-ado.md), ADO создаст новое поле в источнике данных, если это разрешено поставщиком.</span><span class="sxs-lookup"><span data-stu-id="34a50-116">When you call [Update](update-method-ado.md), ADO will create a new field in your data source if allowed by your provider.</span></span>

