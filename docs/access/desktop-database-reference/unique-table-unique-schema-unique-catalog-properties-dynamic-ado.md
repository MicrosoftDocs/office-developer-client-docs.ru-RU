---
title: Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)
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
# <a name="unique-table-unique-schema-unique-catalog-dynamic-properties-ado"></a><span data-ttu-id="2532e-102">Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)</span><span class="sxs-lookup"><span data-stu-id="2532e-102">Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)</span></span>


<span data-ttu-id="2532e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2532e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2532e-104">Позволяет внимательно контролировать изменения определенной базовой таблицы в наборе [записей,](recordset-object-ado.md) сформированном операцией JOIN на нескольких базовых таблицах.</span><span class="sxs-lookup"><span data-stu-id="2532e-104">Enables you to closely control modifications to a particular base table in a [Recordset](recordset-object-ado.md) that was formed by a JOIN operation on multiple base tables.</span></span>

  - <span data-ttu-id="2532e-105">**Уникальная** таблица указывает имя базовой таблицы, в которой разрешены обновления, вставки и удаления.</span><span class="sxs-lookup"><span data-stu-id="2532e-105">**Unique Table** specifies the name of the base table upon which updates, insertions, and deletions are allowed.</span></span>

  - <span data-ttu-id="2532e-106">**Уникальная схема** указывает *схему* или имя владельца таблицы.</span><span class="sxs-lookup"><span data-stu-id="2532e-106">**Unique Schema** specifies the *schema*, or name of the owner of the table.</span></span>

  - <span data-ttu-id="2532e-107">**Уникальный каталог** определяет *каталог или* имя базы данных, содержащей таблицу.</span><span class="sxs-lookup"><span data-stu-id="2532e-107">**Unique Catalog** specifies the *catalog*, or name of the database containing the table.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="2532e-108">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="2532e-108">Settings and return values</span></span>

<span data-ttu-id="2532e-109">Задает или возвращает **строку,** которая является именем таблицы, схемы или каталога.</span><span class="sxs-lookup"><span data-stu-id="2532e-109">Sets or returns a **String** value that is the name of a table, schema, or catalog.</span></span>

## <a name="remarks"></a><span data-ttu-id="2532e-110">Заметки</span><span class="sxs-lookup"><span data-stu-id="2532e-110">Remarks</span></span>

<span data-ttu-id="2532e-111">Желаемая базовая таблица уникально идентифицирована по каталогу, схеме и именам таблиц.</span><span class="sxs-lookup"><span data-stu-id="2532e-111">The desired base table is uniquely identified by its catalog, schema, and table names.</span></span> <span data-ttu-id="2532e-112">При **наборе** свойства "Уникальная таблица" значения  свойств "Уникальная схема" или "Уникальный каталог" используются для поиска базовой таблицы. </span><span class="sxs-lookup"><span data-stu-id="2532e-112">When the **Unique Table** property is set, the values of the **Unique Schema** or **Unique Catalog** properties are used to find the base table.</span></span> <span data-ttu-id="2532e-113">Предполагается, но не обязательно, чтобы либо свойства **Unique Schema,** так и **Unique Catalog** были установлены до того, как будет установлено свойство **"Уникальная** таблица".</span><span class="sxs-lookup"><span data-stu-id="2532e-113">It is intended, but not required, that either or both the **Unique Schema** and **Unique Catalog** properties be set before the **Unique Table** property is set.</span></span>

<span data-ttu-id="2532e-114">Первичный ключ **уникальной таблицы** рассматривается как первичный ключ всего **наборов записей.**</span><span class="sxs-lookup"><span data-stu-id="2532e-114">The primary key of the **Unique Table** is treated as the primary key of the entire **Recordset**.</span></span> <span data-ttu-id="2532e-115">Это ключ, используемый для любого метода, требующего первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="2532e-115">This is the key that is used for any method requiring a primary key.</span></span>

<span data-ttu-id="2532e-116">Несмотря **на то что установлена** уникальная таблица, метод [Delete](delete-method-ado-recordset.md) влияет только на именоваемую таблицу.</span><span class="sxs-lookup"><span data-stu-id="2532e-116">While **Unique Table** is set, the [Delete](delete-method-ado-recordset.md) method affects only the named table.</span></span> <span data-ttu-id="2532e-117">Методы [AddNew,](addnew-method-ado.md) [Resync,](resync-method-ado.md) [Update](update-method-ado.md)и [UpdateBatch](updatebatch-method-ado.md) влияют на все соответствующие базовые таблицы **recordset.**</span><span class="sxs-lookup"><span data-stu-id="2532e-117">The [AddNew](addnew-method-ado.md), [Resync](resync-method-ado.md), [Update](update-method-ado.md), and [UpdateBatch](updatebatch-method-ado.md) methods affect any appropriate underlying base tables of the **Recordset**.</span></span>

<span data-ttu-id="2532e-118">**Уникальная** таблица должна быть указана перед любыми пользовательскими ресинхронизацией.</span><span class="sxs-lookup"><span data-stu-id="2532e-118">**Unique Table** must be specified before doing any custom resynchronizations.</span></span> <span data-ttu-id="2532e-119">Если **уникальная** таблица не указана, свойство [Resync Command](resync-command-property-dynamic-ado.md) не будет действовать.</span><span class="sxs-lookup"><span data-stu-id="2532e-119">If **Unique Table** has not been specified, the [Resync Command](resync-command-property-dynamic-ado.md) property will have no effect.</span></span>

<span data-ttu-id="2532e-120">Ошибка во время работы приводит к невозможности найти уникальную базовую таблицу.</span><span class="sxs-lookup"><span data-stu-id="2532e-120">A run-time error results if a unique base table cannot be found.</span></span>

<span data-ttu-id="2532e-121">Все эти динамические свойства appended to the **Recordset** object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="2532e-121">These dynamic properties are all appended to the **Recordset** object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

