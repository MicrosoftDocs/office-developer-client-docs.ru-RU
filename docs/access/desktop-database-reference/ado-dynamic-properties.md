---
title: Динамические свойства ADO
TOCTitle: ADO Dynamic Properties
ms:assetid: a908bc52-2cb0-89c7-a997-2cde93477e4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249782(v=office.15)
ms:contentKeyID: 48546915
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a35bf0cd62db8f635540bfd1ccd65995b198b46
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877550"
---
# <a name="ado-dynamic-properties"></a><span data-ttu-id="1bf1d-102">Динамические свойства ADO</span><span class="sxs-lookup"><span data-stu-id="1bf1d-102">ADO Dynamic Properties</span></span>


<span data-ttu-id="1bf1d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1bf1d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1bf1d-104">Динамические свойства можно добавить в коллекции [свойств](properties-collection-ado.md) объектов [подключения](connection-object-ado.md), [команда](command-object-ado.md)или [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1bf1d-104">Dynamic properties can be added to the [Properties](properties-collection-ado.md) collections of the [Connection](connection-object-ado.md), [Command](command-object-ado.md), or [Recordset](recordset-object-ado.md) objects.</span></span> <span data-ttu-id="1bf1d-105">Источник данных свойств — это либо поставщик данных, таких как [Поставщик OLE DB для SQL Server](microsoft-ole-db-provider-for-sql-server.md)или поставщика услуг, таких как [Служба курсора для OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md).</span><span class="sxs-lookup"><span data-stu-id="1bf1d-105">The source for these properties is either a data provider, such as the [OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), or a service provider, such as the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md).</span></span> <span data-ttu-id="1bf1d-106">Обратитесь к требуемые данные поставщика или документации поставщика службы Дополнительные сведения о конкретных динамического свойства.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-106">Refer to the appropriate data provider or service provider documentation for more information about a specific dynamic property.</span></span>

<span data-ttu-id="1bf1d-107">[Динамические свойства индекса ADO](ado-dynamic-property-index.md) предоставляет перекрестная ссылка между имена ADO и OLE DB для каждого стандартных OLE DB поставщика динамические свойства.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-107">The [ADO Dynamic Property Index](ado-dynamic-property-index.md) provides a cross-reference between the ADO and OLE DB names for each standard OLE DB provider dynamic property.</span></span>

<span data-ttu-id="1bf1d-108">Следующие свойства динамического представляют интерес и также описаны в источниках, перечисленных выше.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-108">The following dynamic properties are of special interest, and are also documented in the sources mentioned above.</span></span> <span data-ttu-id="1bf1d-109">Специальные функциональные возможности с помощью ADO описана в перечисленных ниже разделах справки ADO.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-109">Special functionality with ADO is documented in the ADO help topics listed below.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1bf1d-110"><a href="optimize-property-dynamic-ado.md">Оптимизация</a></span><span class="sxs-lookup"><span data-stu-id="1bf1d-110"><a href="optimize-property-dynamic-ado.md">Optimize</a></span></span></p></td>
<td><p><span data-ttu-id="1bf1d-111">Указывает, следует ли создавать индекса на это поле.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-111">Specifies whether an index should be created on this field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bf1d-112"><a href="prompt-property-dynamic-ado.md">Запрос</a></span><span class="sxs-lookup"><span data-stu-id="1bf1d-112"><a href="prompt-property-dynamic-ado.md">Prompt</a></span></span></p></td>
<td><p><span data-ttu-id="1bf1d-113">Указывает, следует ли поставщик OLE DB запрашивать у пользователя сведения инициализации.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-113">Specifies whether the OLE DB provider should prompt the user for initialization information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bf1d-114"><a href="reshape-name-property-dynamic-ado.md">Изменить форму имя</a></span><span class="sxs-lookup"><span data-stu-id="1bf1d-114"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span></span></p></td>
<td><p><span data-ttu-id="1bf1d-115">Указывает имя для объекта <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="1bf1d-115">Specifies a name for the <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bf1d-116"><a href="resync-command-property-dynamic-ado.md">Команда синхронизации</a></span><span class="sxs-lookup"><span data-stu-id="1bf1d-116"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span></span></p></td>
<td><p><span data-ttu-id="1bf1d-117">Указывает строку пользовательские команды, метод <strong>выполнить повторную синхронизацию</strong> проблемы для обновления данных в таблице с именем в свойстве динамических <strong>Уникальной таблицы</strong> .</span><span class="sxs-lookup"><span data-stu-id="1bf1d-117">Specifies a user-supplied command string that the <strong>Resync</strong> method issues to refresh the data in the table named in the <strong>Unique Table</strong> dynamic property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bf1d-118"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальной таблицы, уникальные схемы, уникальный каталога</a></span><span class="sxs-lookup"><span data-stu-id="1bf1d-118"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table, Unique Schema, Unique Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="1bf1d-119"><strong>Уникальная таблица</strong> — определяет имя базовая таблица, для которой разрешены обновления, вставки и удаления.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-119"><strong>Unique Table</strong> — specifies the name of the base table upon which updates, insertions, and deletions are allowed.</span></span> <span data-ttu-id="1bf1d-120"><strong>Уникальный схемы</strong> — определяет схему или имя владельца таблицы.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-120"><strong>Unique Schema</strong> — specifies the schema, or name of the owner of the table.</span></span> <span data-ttu-id="1bf1d-121"><strong>Уникальный каталога</strong> — указывает каталог или имя базы данных, содержащий таблицу.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-121"><strong>Unique Catalog</strong> — specifies the catalog, or name of the database containing the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bf1d-122"><a href="update-resync-property-dynamic-ado.md">Обновление повторной синхронизации</a></span><span class="sxs-lookup"><span data-stu-id="1bf1d-122"><a href="update-resync-property-dynamic-ado.md">Update Resync</a></span></span></p></td>
<td><p><span data-ttu-id="1bf1d-123">Указывает, будет ли метод <strong>UpdateBatch</strong> следуют неявных <strong>выполнить повторную синхронизацию</strong> метод операцию и если да, области действия этой операции.</span><span class="sxs-lookup"><span data-stu-id="1bf1d-123">Specifies whether the <strong>UpdateBatch</strong> method is followed by an implicit <strong>Resync</strong> method operation, and if so, the scope of that operation.</span></span></p></td>
</tr>
</tbody>
</table>

