---
title: Метод UpdateBatch (ADO)
TOCTitle: UpdateBatch method (ADO)
ms:assetid: 69e72a65-b637-36fd-d09f-7f81050f71ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249416(v=office.15)
ms:contentKeyID: 48545420
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9d269a9012588a7b82505ac2e28466151715cbb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313578"
---
# <a name="updatebatch-method-ado"></a><span data-ttu-id="ba26a-102">Метод UpdateBatch (ADO)</span><span class="sxs-lookup"><span data-stu-id="ba26a-102">UpdateBatch method (ADO)</span></span>

<span data-ttu-id="ba26a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba26a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba26a-104">Записывает все ожидающие пакетные обновления на диск.</span><span class="sxs-lookup"><span data-stu-id="ba26a-104">Writes all pending batch updates to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba26a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba26a-105">Syntax</span></span>

<span data-ttu-id="ba26a-106">*набор записей*. UpdateBatch*аффектрекордс*</span><span class="sxs-lookup"><span data-stu-id="ba26a-106">*recordset*.UpdateBatch*AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="ba26a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba26a-107">Parameters</span></span>

|<span data-ttu-id="ba26a-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="ba26a-108">Parameter</span></span>|<span data-ttu-id="ba26a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ba26a-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ba26a-110">*аффектрекордс*</span><span class="sxs-lookup"><span data-stu-id="ba26a-110">*AffectRecords*</span></span> |<span data-ttu-id="ba26a-111">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="ba26a-111">Optional.</span></span> <span data-ttu-id="ba26a-112">Значение [аффектенум](affectenum.md) , указывающее количество записей, на которые влияет метод **UpdateBatch** .</span><span class="sxs-lookup"><span data-stu-id="ba26a-112">An [AffectEnum](affectenum.md) value that indicates how many records the **UpdateBatch** method will affect.</span></span>|

## <a name="remarks"></a><span data-ttu-id="ba26a-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="ba26a-113">Remarks</span></span>

<span data-ttu-id="ba26a-114">Используйте метод **UpdateBatch** при изменении объекта **Recordset** в режиме пакетного обновления для передачи всех изменений, внесенных в объект **Recordset** в базовую базу данных.</span><span class="sxs-lookup"><span data-stu-id="ba26a-114">Use the **UpdateBatch** method when modifying a **Recordset** object in batch update mode to transmit all changes made in a **Recordset** object to the underlying database.</span></span>

<span data-ttu-id="ba26a-115">Если объект **Recordset** поддерживает пакетное обновление, можно кэшировать несколько изменений в одну или несколько записей локально, пока не будет вызван метод **UpdateBatch** .</span><span class="sxs-lookup"><span data-stu-id="ba26a-115">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the **UpdateBatch** method.</span></span> <span data-ttu-id="ba26a-116">Если вы редактируете текущую запись или добавляете новую запись при вызове метода **UpdateBatch** , ADO автоматически вызывает метод [Update](update-method-ado.md) для сохранения всех ожидающих изменений в текущей записи, прежде чем передавать пакетные изменения поставщику.</span><span class="sxs-lookup"><span data-stu-id="ba26a-116">If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the [Update](update-method-ado.md) method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span> <span data-ttu-id="ba26a-117">Пакетное обновление следует использовать только с помощью набора ключей или только статического курсора.</span><span class="sxs-lookup"><span data-stu-id="ba26a-117">You should use batch updating with either a keyset or static cursor only.</span></span>

> [!NOTE]
> <span data-ttu-id="ba26a-118">Указание **адаффектграуп** в качестве значения для этого параметра приведет к ошибке при отсутствии отображаемых записей в текущем **наборе записей** (например, в фильтре, для которого не найдено записей).</span><span class="sxs-lookup"><span data-stu-id="ba26a-118">Specifying **adAffectGroup** as the value for this parameter will result in an error when there are no visible records in the current **Recordset** (such as a filter for which no records match).</span></span>

<span data-ttu-id="ba26a-119">Если при попытке передать изменения для любой или всех записей происходит сбой из-за конфликта с базовыми данными (например, запись уже была удалена другим пользователем), то поставщик возвращает предупреждения для коллекции [Errors](errors-collection-ado.md) и возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="ba26a-119">If the attempt to transmit changes fails for any or all records because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection and a run-time error occurs.</span></span> <span data-ttu-id="ba26a-120">Используйте свойство [Filter](filter-property-ado.md) (**адфилтераффектедрекордс**) и свойство [Status](status-property-ado-recordset.md) для обнаружения записей с конфликтами.</span><span class="sxs-lookup"><span data-stu-id="ba26a-120">Use the [Filter](filter-property-ado.md) property (**adFilterAffectedRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

<span data-ttu-id="ba26a-121">Чтобы отменить все ожидающие пакетные обновления, используйте метод [CancelBatch](cancelbatch-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="ba26a-121">To cancel all pending batch updates, use the [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="ba26a-122">Если задана [уникальная таблица](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) и динамические свойства повторной [синхронизации обновления](update-resync-property-dynamic-ado.md) , а **набор записей** является результатом выполнения операции присоединения к нескольким таблицам, то при выполнении метода **UpdateBatch** неявно следует использовать метод [Resync](resync-method-ado.md) в зависимости от параметров свойства **Resync** .</span><span class="sxs-lookup"><span data-stu-id="ba26a-122">If the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and [Update Resync](update-resync-property-dynamic-ado.md) dynamic properties are set, and the **Recordset** is the result of executing a JOIN operation on multiple tables, then the execution of the **UpdateBatch** method is implicitly followed by the [Resync](resync-method-ado.md) method depending on the settings of the **Update Resync** property.</span></span>

<span data-ttu-id="ba26a-123">Порядок, в котором отдельные обновления пакета выполняются в источнике данных, не обязательно совпадает с порядком, в котором они были выполнены для локального **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="ba26a-123">The order in which the individual updates of a batch are performed on the data source is not necessarily the same as the order in which they were performed on the local **Recordset**.</span></span> <span data-ttu-id="ba26a-124">Порядок обновления зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="ba26a-124">Update order is dependent upon the provider.</span></span> <span data-ttu-id="ba26a-125">Это необходимо учитывать при кодировании обновлений, связанных друг с другом, таких как ограничения внешнего ключа при вставке или обновлении.</span><span class="sxs-lookup"><span data-stu-id="ba26a-125">Take this into account when coding updates that are related to one another, such as foreign key constraints on an insert or update.</span></span>

