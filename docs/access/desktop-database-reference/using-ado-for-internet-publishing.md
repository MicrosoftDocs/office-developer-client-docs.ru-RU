---
title: Using ADO for Internet Publishing
TOCTitle: Using ADO for Internet Publishing
ms:assetid: 1e829783-fc12-e303-6f12-2df1ca96cb0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248975(v=office.15)
ms:contentKeyID: 48543622
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ae8341151c7bf7d90585794061647ba33a5c4ea7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305903"
---
# <a name="using-ado-for-internet-publishing"></a><span data-ttu-id="5ee45-102">Использование ADO для публикации в Интернете</span><span class="sxs-lookup"><span data-stu-id="5ee45-102">Using ADO for Internet publishing</span></span>


<span data-ttu-id="5ee45-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5ee45-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="5ee45-104">[Поставщик OLE DB для публикации](the-ole-db-provider-for-internet-publishing.md) в Интернете показывает конкретный пример доступа к разнородным данным с помощью ADO.</span><span class="sxs-lookup"><span data-stu-id="5ee45-104">[The OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md) shows a specific example of accessing heterogeneous data with ADO.</span></span> <span data-ttu-id="5ee45-105">Хотя в примерах в этом разделе используется поставщик публикации в Интернете, принципы, которые демонстрируются при использовании ADO с другими поставщиками, должны быть похожи на разнородные данные, такие как поставщик в хранилище электронной почты.</span><span class="sxs-lookup"><span data-stu-id="5ee45-105">While the examples in this section will be specific to using the Internet Publishing Provider, the principles demonstrated should be similar when using ADO with other providers to heterogeneous data, such as a provider to an email store.</span></span>

## <a name="urls"></a><span data-ttu-id="5ee45-106">URL-адреса</span><span class="sxs-lookup"><span data-stu-id="5ee45-106">URLs</span></span>

<span data-ttu-id="5ee45-107">Url-адреса можно использовать в качестве альтернативы строкам подключения и тексту команды для указания источников данных и расположения файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="5ee45-107">Uniform Resource Locators (URLs) can be used as an alternative to connection strings and command text to specify data sources and the location of files and directories.</span></span> <span data-ttu-id="5ee45-108">Вы можете использовать URL-адреса с существующими объектами [Connection](connection-object-ado.md) и **Recordset,** а также с объектами **Record** и **Stream.**</span><span class="sxs-lookup"><span data-stu-id="5ee45-108">You can use URLs with the existing [Connection](connection-object-ado.md) and **Recordset** objects as well as with the **Record** and **Stream** objects.</span></span>

<span data-ttu-id="5ee45-109">Дополнительные сведения об использовании URL-адресов см. в [сведениях об абсолютных и относительных URL-адресах.](absolute-and-relative-urls.md)</span><span class="sxs-lookup"><span data-stu-id="5ee45-109">For more information about using URLs, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span>

## <a name="record-fields"></a><span data-ttu-id="5ee45-110">Поля записей</span><span class="sxs-lookup"><span data-stu-id="5ee45-110">Record Fields</span></span>

<span data-ttu-id="5ee45-111">Различие между разнородными и однородными данными состоит в том, что для первой строки данных или записи может быть разный набор столбцов или полей. </span><span class="sxs-lookup"><span data-stu-id="5ee45-111">The distinguishing difference between heterogeneous data and homogeneous data is that for the former, each row of data, or **Record**, can have a different set of columns, or **Fields**.</span></span> <span data-ttu-id="5ee45-112">Для однородных данных каждая строка имеет одинаковый набор столбцов.</span><span class="sxs-lookup"><span data-stu-id="5ee45-112">For homogeneous data, each row has the same set of columns.</span></span> <span data-ttu-id="5ee45-113">Дополнительные сведения о полях, характерных для поставщика интернет-публикации, см. в Provider-Supplied ["Записи" и "Provider-Supplied".](records-and-provider-supplied-fields.md)</span><span class="sxs-lookup"><span data-stu-id="5ee45-113">For more information about the fields specific to the Internet Publishing Provider, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>

## <a name="appending-new-fields"></a><span data-ttu-id="5ee45-114">Appending New Fields</span><span class="sxs-lookup"><span data-stu-id="5ee45-114">Appending New Fields</span></span>

<span data-ttu-id="5ee45-115">Несколько объектов ADO были улучшены для работы в сочетании с объектами **Record** и **Stream.**</span><span class="sxs-lookup"><span data-stu-id="5ee45-115">Several ADO objects have been enhanced to work in conjunction with **Record** and **Stream** objects.</span></span>

  - <span data-ttu-id="5ee45-116">Метод [Append коллекции](append-method-ado.md) [Fields,](fields-collection-ado.md) который создает и добавляет объект [Field](field-object-ado.md) в коллекцию, также может указывать значение **поля.**</span><span class="sxs-lookup"><span data-stu-id="5ee45-116">The [Fields](fields-collection-ado.md) collection [Append](append-method-ado.md) method, which creates and adds a [Field](field-object-ado.md) object to the collection, can also specify the value of the **Field**.</span></span>

  - <span data-ttu-id="5ee45-117">Метод [Update](update-method-ado.md) завершает добавление или удаление полей в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="5ee45-117">The [Update](update-method-ado.md) method finalizes the addition or deletion of fields to the collection.</span></span>

  - <span data-ttu-id="5ee45-118">В качестве ярлыка и альтернативы методу **Append** можно создать поля, просто назначив значение неопределененным или ранее удаленным полям.</span><span class="sxs-lookup"><span data-stu-id="5ee45-118">As a shortcut and alternative to the **Append** method, you may create fields by simply assigning a value to an undefined or previously deleted field.</span></span>

## <a name="see-also"></a><span data-ttu-id="5ee45-119">См. также</span><span class="sxs-lookup"><span data-stu-id="5ee45-119">See also</span></span>

- [<span data-ttu-id="5ee45-120">Темы сценария публикации в Интернете</span><span class="sxs-lookup"><span data-stu-id="5ee45-120">Internet Publishing Scenario topics</span></span>](internet-publishing-scenario.md)
