---
title: Уникальной таблицы, уникальные схемы динамические свойства уникальный каталога (ADO)
TOCTitle: Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)
ms:assetid: e6374782-755b-322b-21de-6d6a386dcd98
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250169(v=office.15)
ms:contentKeyID: 48548374
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b2c3c87a820638b74e74c513443261e052e2c4d7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919432"
---
# <a name="unique-table-unique-schema-unique-catalog-dynamic-properties-ado"></a><span data-ttu-id="81a62-102">Уникальной таблицы, уникальные схемы динамические свойства уникальный каталога (ADO)</span><span class="sxs-lookup"><span data-stu-id="81a62-102">Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)</span></span>


<span data-ttu-id="81a62-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="81a62-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="81a62-104">Позволяет тесно управления изменения определенного базовые таблицы в [набор записей](recordset-object-ado.md) , которая была создана с помощью операции ОБЪЕДИНЕНИЯ на нескольких базовых таблиц.</span><span class="sxs-lookup"><span data-stu-id="81a62-104">Enables you to closely control modifications to a particular base table in a [Recordset](recordset-object-ado.md) that was formed by a JOIN operation on multiple base tables.</span></span>

  - <span data-ttu-id="81a62-105">**Уникальная таблица** указывает имя базовая таблица после обновления, вставки и удаления, разрешены.</span><span class="sxs-lookup"><span data-stu-id="81a62-105">**Unique Table** specifies the name of the base table upon which updates, insertions, and deletions are allowed.</span></span>

  - <span data-ttu-id="81a62-106">**Уникальный схемы** указывает *схемы*или имя владельца таблицы.</span><span class="sxs-lookup"><span data-stu-id="81a62-106">**Unique Schema** specifies the *schema*, or name of the owner of the table.</span></span>

  - <span data-ttu-id="81a62-107">**Уникальный каталог** указывает *каталог*или имя базы данных, содержащий таблицу.</span><span class="sxs-lookup"><span data-stu-id="81a62-107">**Unique Catalog** specifies the *catalog*, or name of the database containing the table.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="81a62-108">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="81a62-108">Settings and return values</span></span>

<span data-ttu-id="81a62-109">Задает или возвращает значение типа **String** , — это имя таблицы, схемы или каталога.</span><span class="sxs-lookup"><span data-stu-id="81a62-109">Sets or returns a **String** value that is the name of a table, schema, or catalog.</span></span>

## <a name="remarks"></a><span data-ttu-id="81a62-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="81a62-110">Remarks</span></span>

<span data-ttu-id="81a62-111">Требуемое базовая таблица однозначно определяется его каталога, схемы и имена таблиц.</span><span class="sxs-lookup"><span data-stu-id="81a62-111">The desired base table is uniquely identified by its catalog, schema, and table names.</span></span> <span data-ttu-id="81a62-112">Если свойство **Уникальной таблицы** , значения свойств **Уникальный схемы** и **Уникальные каталогов** используются для поиска базовая таблица.</span><span class="sxs-lookup"><span data-stu-id="81a62-112">When the **Unique Table** property is set, the values of the **Unique Schema** or **Unique Catalog** properties are used to find the base table.</span></span> <span data-ttu-id="81a62-113">Он предназначен, но не требуется, что один или оба свойства **Уникальный схемы** и **Уникальные каталога** задать перед свойству **Уникальной таблицы** .</span><span class="sxs-lookup"><span data-stu-id="81a62-113">It is intended, but not required, that either or both the **Unique Schema** and **Unique Catalog** properties be set before the **Unique Table** property is set.</span></span>

<span data-ttu-id="81a62-114">Первичный ключ в **Таблице уникальный** обрабатывается как первичный ключ всего **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="81a62-114">The primary key of the **Unique Table** is treated as the primary key of the entire **Recordset**.</span></span> <span data-ttu-id="81a62-115">Это ключ, используемый для любого метода, требующие первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="81a62-115">This is the key that is used for any method requiring a primary key.</span></span>

<span data-ttu-id="81a62-116">Во время **Уникальной таблицы** имеет значение, метод [Delete](delete-method-ado-recordset.md) действует только именованные таблицу.</span><span class="sxs-lookup"><span data-stu-id="81a62-116">While **Unique Table** is set, the [Delete](delete-method-ado-recordset.md) method affects only the named table.</span></span> <span data-ttu-id="81a62-117">Методы [AddNew](addnew-method-ado.md), [выполнить повторную синхронизацию](resync-method-ado.md), [обновления](update-method-ado.md)и [UpdateBatch](updatebatch-method-ado.md) влияет на все соответствующие базовые таблицы из **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="81a62-117">The [AddNew](addnew-method-ado.md), [Resync](resync-method-ado.md), [Update](update-method-ado.md), and [UpdateBatch](updatebatch-method-ado.md) methods affect any appropriate underlying base tables of the **Recordset**.</span></span>

<span data-ttu-id="81a62-118">Перед выполнением любого настраиваемого нарушением должен быть указан **Уникальной таблицы** .</span><span class="sxs-lookup"><span data-stu-id="81a62-118">**Unique Table** must be specified before doing any custom resynchronizations.</span></span> <span data-ttu-id="81a62-119">Если **Уникальной таблицы** не указан, [Команда выполнить повторную синхронизацию](resync-command-property-dynamic-ado.md) свойство не будет действовать.</span><span class="sxs-lookup"><span data-stu-id="81a62-119">If **Unique Table** has not been specified, the [Resync Command](resync-command-property-dynamic-ado.md) property will have no effect.</span></span>

<span data-ttu-id="81a62-120">Если не удается найти уникальный базовая таблица приводит к ошибке времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="81a62-120">A run-time error results if a unique base table cannot be found.</span></span>

<span data-ttu-id="81a62-121">Эти динамические свойства всех присоединяются к коллекции [свойств](properties-collection-ado.md) объекта **набора записей** при [CursorLocation](cursorlocation-property-ado.md) задано значение **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="81a62-121">These dynamic properties are all appended to the **Recordset** object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

