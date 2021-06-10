---
title: Динамические свойства ADO
TOCTitle: ADO dynamic properties
ms:assetid: a908bc52-2cb0-89c7-a997-2cde93477e4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249782(v=office.15)
ms:contentKeyID: 48546915
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fae0df2a4cc5c9de585d2b101e9fa31cb6a0a545
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281717"
---
# <a name="ado-dynamic-properties"></a><span data-ttu-id="67eab-102">Динамические свойства ADO</span><span class="sxs-lookup"><span data-stu-id="67eab-102">ADO dynamic properties</span></span>

<span data-ttu-id="67eab-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="67eab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="67eab-104">Динамические свойства могут быть добавлены в коллекции [Свойств](properties-collection-ado.md) объектов [Подключения,](connection-object-ado.md) [Команды](command-object-ado.md)или [Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="67eab-104">Dynamic properties can be added to the [Properties](properties-collection-ado.md) collections of the [Connection](connection-object-ado.md), [Command](command-object-ado.md), or [Recordset](recordset-object-ado.md) objects.</span></span> <span data-ttu-id="67eab-105">Источником этих свойств является либо поставщик данных, например поставщик [OLE DB](microsoft-ole-db-provider-for-sql-server.md)для SQL Server, либо поставщик услуг, например служба [Microsoft Cursor для OLE DB.](microsoft-cursor-service-for-ole-db-ado-service-component.md)</span><span class="sxs-lookup"><span data-stu-id="67eab-105">The source for these properties is either a data provider, such as the [OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), or a service provider, such as the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md).</span></span> <span data-ttu-id="67eab-106">Дополнительные сведения о конкретном динамическом свойстве обратитесь к соответствующему поставщику данных или документации поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="67eab-106">Refer to the appropriate data provider or service provider documentation for more information about a specific dynamic property.</span></span>

<span data-ttu-id="67eab-107">Индекс [динамического свойства ADO](ado-dynamic-property-index.md) предоставляет перекрестную ссылку между именами ADO и OLE DB для каждого стандартного динамического свойства поставщика OLE DB.</span><span class="sxs-lookup"><span data-stu-id="67eab-107">The [ADO Dynamic Property Index](ado-dynamic-property-index.md) provides a cross-reference between the ADO and OLE DB names for each standard OLE DB provider dynamic property.</span></span>

<span data-ttu-id="67eab-108">Особый интерес имеют следующие динамические свойства, которые также описаны в указанных выше источниках.</span><span class="sxs-lookup"><span data-stu-id="67eab-108">The following dynamic properties are of special interest, and are also documented in the sources mentioned above.</span></span> <span data-ttu-id="67eab-109">Специальные функции с ADO описаны в ниже перечисленных ниже темах справки ADO.</span><span class="sxs-lookup"><span data-stu-id="67eab-109">Special functionality with ADO is documented in the ADO help topics listed below.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="67eab-110">Динамическое свойство</span><span class="sxs-lookup"><span data-stu-id="67eab-110">Dynamic property</span></span></th>
<th><span data-ttu-id="67eab-111">Description</span><span class="sxs-lookup"><span data-stu-id="67eab-111">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67eab-112"><a href="optimize-property-dynamic-ado.md">Оптимизация</a></span><span class="sxs-lookup"><span data-stu-id="67eab-112"><a href="optimize-property-dynamic-ado.md">Optimize</a></span></span></p></td>
<td><p><span data-ttu-id="67eab-113">Указывает, следует ли создавать индекс в этом поле.</span><span class="sxs-lookup"><span data-stu-id="67eab-113">Specifies whether an index should be created on this field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67eab-114"><a href="prompt-property-dynamic-ado.md">Prompt</a></span><span class="sxs-lookup"><span data-stu-id="67eab-114"><a href="prompt-property-dynamic-ado.md">Prompt</a></span></span></p></td>
<td><p><span data-ttu-id="67eab-115">Указывает, должен ли поставщик OLE DB подсказыть пользователю сведения о инициализации.</span><span class="sxs-lookup"><span data-stu-id="67eab-115">Specifies whether the OLE DB provider should prompt the user for initialization information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67eab-116"><a href="reshape-name-property-dynamic-ado.md">Переописываю имя</a></span><span class="sxs-lookup"><span data-stu-id="67eab-116"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span></span></p></td>
<td><p><span data-ttu-id="67eab-117">Указывает имя объекта <strong>Recordset.</strong></span><span class="sxs-lookup"><span data-stu-id="67eab-117">Specifies a name for the <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67eab-118"><a href="resync-command-property-dynamic-ado.md">Команда Resync</a></span><span class="sxs-lookup"><span data-stu-id="67eab-118"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span></span></p></td>
<td><p><span data-ttu-id="67eab-119">Указывает командную строку, предоставленную пользователем, которую метод <strong>Resync</strong> выдает для обновления данных в таблице, указанной в динамическом свойстве <strong>Unique Table.</strong></span><span class="sxs-lookup"><span data-stu-id="67eab-119">Specifies a user-supplied command string that the <strong>Resync</strong> method issues to refresh the data in the table named in the <strong>Unique Table</strong> dynamic property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67eab-120"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальная таблица, уникальная схема, уникальный каталог</a></span><span class="sxs-lookup"><span data-stu-id="67eab-120"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table, Unique Schema, Unique Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="67eab-121"><strong>Уникальная</strong> таблица указывает имя базовой таблицы, на которую допускаются обновления, вставки и удаления.</span><span class="sxs-lookup"><span data-stu-id="67eab-121"><strong>Unique Table</strong> — specifies the name of the base table upon which updates, insertions, and deletions are allowed.</span></span><br/><br/><span data-ttu-id="67eab-122"><strong>Уникальная схема</strong> — указывает схему или имя владельца таблицы.</span><span class="sxs-lookup"><span data-stu-id="67eab-122"><strong>Unique Schema</strong> — specifies the schema, or name of the owner of the table.</span></span><br/><br/><span data-ttu-id="67eab-123"><strong>Уникальный каталог</strong> — указывает каталог или имя базы данных, содержащей таблицу.</span><span class="sxs-lookup"><span data-stu-id="67eab-123"><strong>Unique Catalog</strong> — specifies the catalog, or name of the database containing the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67eab-124"><a href="update-resync-property-dynamic-ado.md">Обновление Resync</a></span><span class="sxs-lookup"><span data-stu-id="67eab-124"><a href="update-resync-property-dynamic-ado.md">Update Resync</a></span></span></p></td>
<td><p><span data-ttu-id="67eab-125">Указывает, следует ли <strong>методу UpdateBatch</strong> неявная операция метода <strong>Resync</strong> и если да, то область этой операции.</span><span class="sxs-lookup"><span data-stu-id="67eab-125">Specifies whether the <strong>UpdateBatch</strong> method is followed by an implicit <strong>Resync</strong> method operation, and if so, the scope of that operation.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

