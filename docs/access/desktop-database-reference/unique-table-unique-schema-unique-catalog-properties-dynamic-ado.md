---
title: Уникальная таблица, уникальная схема, динамические свойства каталога Unique (ADO)
TOCTitle: Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)
ms:assetid: e6374782-755b-322b-21de-6d6a386dcd98
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250169(v=office.15)
ms:contentKeyID: 48548374
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5f4bf93afc200edd88e89cf5d4e90435c2476942
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313750"
---
# <a name="unique-table-unique-schema-unique-catalog-dynamic-properties-ado"></a><span data-ttu-id="e3fe2-102">Уникальная таблица, уникальная схема, динамические свойства каталога Unique (ADO)</span><span class="sxs-lookup"><span data-stu-id="e3fe2-102">Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)</span></span>


<span data-ttu-id="e3fe2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e3fe2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e3fe2-104">Позволяет тесно контролировать изменения в определенной базовой таблице в [наборе записей](recordset-object-ado.md) , созданном ОПЕРАЦИей JOIN с несколькими базовыми таблицами.</span><span class="sxs-lookup"><span data-stu-id="e3fe2-104">Enables you to closely control modifications to a particular base table in a [Recordset](recordset-object-ado.md) that was formed by a JOIN operation on multiple base tables.</span></span>

  - <span data-ttu-id="e3fe2-105">**Уникальная таблица** указывает имя базовой таблицы, для которой разрешены обновления, вставки и удаления.</span><span class="sxs-lookup"><span data-stu-id="e3fe2-105">**Unique Table** specifies the name of the base table upon which updates, insertions, and deletions are allowed.</span></span>

  - <span data-ttu-id="e3fe2-106">**Уникальная схема** указывает *схему*или имя владельца таблицы.</span><span class="sxs-lookup"><span data-stu-id="e3fe2-106">**Unique Schema** specifies the *schema*, or name of the owner of the table.</span></span>

  - <span data-ttu-id="e3fe2-107">**Уникальный каталог** указывает *Каталог*или имя базы данных, содержащей таблицу.</span><span class="sxs-lookup"><span data-stu-id="e3fe2-107">**Unique Catalog** specifies the *catalog*, or name of the database containing the table.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="e3fe2-108">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e3fe2-108">Settings and return values</span></span>

<span data-ttu-id="e3fe2-109">Задает или возвращает **строковое** значение, которое представляет собой имя таблицы, схемы или каталога.</span><span class="sxs-lookup"><span data-stu-id="e3fe2-109">Sets or returns a **String** value that is the name of a table, schema, or catalog.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3fe2-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="e3fe2-110">Remarks</span></span>

<span data-ttu-id="e3fe2-111">Нужная базовая таблица уникально идентифицируется по имени каталога, схемы и таблиц.</span><span class="sxs-lookup"><span data-stu-id="e3fe2-111">The desired base table is uniquely identified by its catalog, schema, and table names.</span></span> <span data-ttu-id="e3fe2-112">Если задано свойство **UNIQUE Table** , то для поиска базовой таблицы используются значения свойств **UNIQUE Schema** или **UNIQUE Catalog** .</span><span class="sxs-lookup"><span data-stu-id="e3fe2-112">When the **Unique Table** property is set, the values of the **Unique Schema** or **Unique Catalog** properties are used to find the base table.</span></span> <span data-ttu-id="e3fe2-113">Он предназначен (но не обязательно), который задается как для уникальной **схемы** , так и для **уникальных свойств каталога** , прежде чем будет задано свойство **UNIQUE Table** .</span><span class="sxs-lookup"><span data-stu-id="e3fe2-113">It is intended, but not required, that either or both the **Unique Schema** and **Unique Catalog** properties be set before the **Unique Table** property is set.</span></span>

<span data-ttu-id="e3fe2-114">Первичный ключ **уникальной таблицы** рассматривается как первичный ключ всего **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="e3fe2-114">The primary key of the **Unique Table** is treated as the primary key of the entire **Recordset**.</span></span> <span data-ttu-id="e3fe2-115">Это ключ, используемый для любого метода, для которого требуется первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="e3fe2-115">This is the key that is used for any method requiring a primary key.</span></span>

<span data-ttu-id="e3fe2-116">Если задана **уникальная таблица** , метод [Delete](delete-method-ado-recordset.md) влияет только на именованную таблицу.</span><span class="sxs-lookup"><span data-stu-id="e3fe2-116">While **Unique Table** is set, the [Delete](delete-method-ado-recordset.md) method affects only the named table.</span></span> <span data-ttu-id="e3fe2-117">Методы [AddNew](addnew-method-ado.md), [Resync](resync-method-ado.md), [Update](update-method-ado.md)и [UpdateBatch](updatebatch-method-ado.md) влияют на соответствующие базовые таблицы **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="e3fe2-117">The [AddNew](addnew-method-ado.md), [Resync](resync-method-ado.md), [Update](update-method-ado.md), and [UpdateBatch](updatebatch-method-ado.md) methods affect any appropriate underlying base tables of the **Recordset**.</span></span>

<span data-ttu-id="e3fe2-118">Перед выполнением любых пользовательских повторных синхронизаций необходимо указать **уникальНую таблицу** .</span><span class="sxs-lookup"><span data-stu-id="e3fe2-118">**Unique Table** must be specified before doing any custom resynchronizations.</span></span> <span data-ttu-id="e3fe2-119">Если не указана **уникальная таблица** , свойство [Command Resync](resync-command-property-dynamic-ado.md) не будет иметь никакого действия.</span><span class="sxs-lookup"><span data-stu-id="e3fe2-119">If **Unique Table** has not been specified, the [Resync Command](resync-command-property-dynamic-ado.md) property will have no effect.</span></span>

<span data-ttu-id="e3fe2-120">Если не удается найти уникальную базовую таблицу, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="e3fe2-120">A run-time error results if a unique base table cannot be found.</span></span>

<span data-ttu-id="e3fe2-121">Эти динамические свойства добавляются в коллекцию [свойств](properties-collection-ado.md) объекта **Recordset** , если для свойства [CursorLocation](cursorlocation-property-ado.md) задано значение **адусеклиент**.</span><span class="sxs-lookup"><span data-stu-id="e3fe2-121">These dynamic properties are all appended to the **Recordset** object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

