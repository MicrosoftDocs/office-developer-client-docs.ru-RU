---
title: Метод UpdateBatch (ADO)
TOCTitle: UpdateBatch method (ADO)
ms:assetid: 69e72a65-b637-36fd-d09f-7f81050f71ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249416(v=office.15)
ms:contentKeyID: 48545420
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2e998bb49fab57927a8bb233d9eeb3245a1a3876
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929939"
---
# <a name="updatebatch-method-ado"></a><span data-ttu-id="85356-102">Метод UpdateBatch (ADO)</span><span class="sxs-lookup"><span data-stu-id="85356-102">UpdateBatch method (ADO)</span></span>


<span data-ttu-id="85356-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="85356-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="85356-104">Записывает все ожидающие пакета обновления на диск.</span><span class="sxs-lookup"><span data-stu-id="85356-104">Writes all pending batch updates to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="85356-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85356-105">Syntax</span></span>

<span data-ttu-id="85356-106">*набор записей*. UpdateBatch*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="85356-106">*recordset*.UpdateBatch*AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="85356-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="85356-107">Parameters</span></span>

  - <span data-ttu-id="85356-108">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="85356-108">*AffectRecords*</span></span>

  - <span data-ttu-id="85356-109">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="85356-109">Optional.</span></span> <span data-ttu-id="85356-110">От [AffectEnum](affectenum.md) значение, которое указывает, сколько записей влияет на метод **UpdateBatch** .</span><span class="sxs-lookup"><span data-stu-id="85356-110">An [AffectEnum](affectenum.md) value that indicates how many records the **UpdateBatch** method will affect.</span></span>

## <a name="remarks"></a><span data-ttu-id="85356-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="85356-111">Remarks</span></span>

<span data-ttu-id="85356-112">Используйте метод **UpdateBatch** при изменении объекта **набора записей** в пакетном режиме обновления для передачи все изменения, внесенные в объект **набора записей** в основной базе данных.</span><span class="sxs-lookup"><span data-stu-id="85356-112">Use the **UpdateBatch** method when modifying a **Recordset** object in batch update mode to transmit all changes made in a **Recordset** object to the underlying database.</span></span>

<span data-ttu-id="85356-113">Если объект **набора записей** поддерживает пакетного обновления, можно кэшировать внесение нескольких изменений в одну или несколько записей локально до вызова метода **UpdateBatch** .</span><span class="sxs-lookup"><span data-stu-id="85356-113">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the **UpdateBatch** method.</span></span> <span data-ttu-id="85356-114">При изменении текущей записи или добавления новой записи при вызове метода **UpdateBatch** , ADO автоматически будет вызвать метод [Update](update-method-ado.md) для сохранения всех ожидающих изменений в текущей записи перед передачей пакетные изменения Поставщик.</span><span class="sxs-lookup"><span data-stu-id="85356-114">If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the [Update](update-method-ado.md) method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span> <span data-ttu-id="85356-115">Следует использовать пакетного обновления с набором ключей или статических текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="85356-115">You should use batch updating with either a keyset or static cursor only.</span></span>


> [!NOTE]
> <P><span data-ttu-id="85356-116">Указание <STRONG>adAffectGroup</STRONG> в качестве значения для этого параметра приведет к ошибку при нет видимых записей в текущего <STRONG>набора записей</STRONG> (например, фильтр, для которого нет записей, соответствующих).</span><span class="sxs-lookup"><span data-stu-id="85356-116">Specifying <STRONG>adAffectGroup</STRONG> as the value for this parameter will result in an error when there are no visible records in the current <STRONG>Recordset</STRONG> (such as a filter for which no records match).</span></span></P>



<span data-ttu-id="85356-117">В случае сбоя попытка передать изменения для некоторых или всех записей из-за конфликта с базовыми данными (например, запись уже была удалена другим пользователем), поставщик возвращает предупреждения семейство [Errors](errors-collection-ado.md) и возникает ошибка времени выполнения .</span><span class="sxs-lookup"><span data-stu-id="85356-117">If the attempt to transmit changes fails for any or all records because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection and a run-time error occurs.</span></span> <span data-ttu-id="85356-118">Используйте свойство [фильтра](filter-property-ado.md) (**adFilterAffectedRecords**) и свойство [состояние](status-property-ado-recordset.md) для поиска записей с конфликтами.</span><span class="sxs-lookup"><span data-stu-id="85356-118">Use the [Filter](filter-property-ado.md) property (**adFilterAffectedRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

<span data-ttu-id="85356-119">Чтобы отменить все ожидающие пакета обновления, используйте метод [CancelBatch](cancelbatch-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="85356-119">To cancel all pending batch updates, use the [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="85356-120">Если заданы свойства динамического [Уникальной таблицы](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) и [Выполнить повторную синхронизацию обновления](update-resync-property-dynamic-ado.md) и **записей** результат выполнения операции СОЕДИНЕНИЯ на несколько таблиц, то выполнение метода **UpdateBatch** неявно следуют Метод [выполнить повторную синхронизацию](resync-method-ado.md) в зависимости от параметров свойства **Обновления выполнить повторную синхронизацию** .</span><span class="sxs-lookup"><span data-stu-id="85356-120">If the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and [Update Resync](update-resync-property-dynamic-ado.md) dynamic properties are set, and the **Recordset** is the result of executing a JOIN operation on multiple tables, then the execution of the **UpdateBatch** method is implicitly followed by the [Resync](resync-method-ado.md) method depending on the settings of the **Update Resync** property.</span></span>

<span data-ttu-id="85356-121">Порядок, в котором отдельные обновления пакета выполняются в источнике данных не обязательно то же, что порядок, в котором они были созданы на локальном **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="85356-121">The order in which the individual updates of a batch are performed on the data source is not necessarily the same as the order in which they were performed on the local **Recordset**.</span></span> <span data-ttu-id="85356-122">Порядок обновления зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="85356-122">Update order is dependent upon the provider.</span></span> <span data-ttu-id="85356-123">Это учитывать при программировании обновлений, которые связаны с друг с другом, такие как ограничения внешнего ключа при вставке или обновлении.</span><span class="sxs-lookup"><span data-stu-id="85356-123">Take this into account when coding updates that are related to one another, such as foreign key constraints on an insert or update.</span></span>

