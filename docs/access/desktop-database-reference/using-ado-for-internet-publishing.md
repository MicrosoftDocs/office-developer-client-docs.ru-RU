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
# <a name="using-ado-for-internet-publishing"></a><span data-ttu-id="02a6d-102">Использование ADO для публикации в Интернете</span><span class="sxs-lookup"><span data-stu-id="02a6d-102">Using ADO for Internet publishing</span></span>


<span data-ttu-id="02a6d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="02a6d-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="02a6d-104">[Поставщик OLE DB для публикации в Интернете](the-ole-db-provider-for-internet-publishing.md) показывает конкретный пример доступа к гетерогенным данным с помощью ADO.</span><span class="sxs-lookup"><span data-stu-id="02a6d-104">[The OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md) shows a specific example of accessing heterogeneous data with ADO.</span></span> <span data-ttu-id="02a6d-105">В примерах, приведенных в этом разделе, будут относиться к использованию поставщика публикации в Интернете, при использовании ADO с другими поставщиками для гетерогенных данных, таких как поставщик, в хранилище электронной почты, демонстрируются аналогичные принципы.</span><span class="sxs-lookup"><span data-stu-id="02a6d-105">While the examples in this section will be specific to using the Internet Publishing Provider, the principles demonstrated should be similar when using ADO with other providers to heterogeneous data, such as a provider to an email store.</span></span>

## <a name="urls"></a><span data-ttu-id="02a6d-106">URL-адреса</span><span class="sxs-lookup"><span data-stu-id="02a6d-106">URLs</span></span>

<span data-ttu-id="02a6d-107">Универсальные указатели ресурсов (URL-адреса) можно использовать в качестве альтернативы строкам подключения и тексту команды для указания источников данных и расположения файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="02a6d-107">Uniform Resource Locators (URLs) can be used as an alternative to connection strings and command text to specify data sources and the location of files and directories.</span></span> <span data-ttu-id="02a6d-108">Вы можете использовать URL-адреса с существующими объектами [Connection](connection-object-ado.md) и **Recordset** , а также с объектами **Record** и **Stream** .</span><span class="sxs-lookup"><span data-stu-id="02a6d-108">You can use URLs with the existing [Connection](connection-object-ado.md) and **Recordset** objects as well as with the **Record** and **Stream** objects.</span></span>

<span data-ttu-id="02a6d-109">Дополнительные сведения об использовании URL-адресов приведены в разделе [абсолютные и ОтносительНые URL-адреса](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="02a6d-109">For more information about using URLs, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span>

## <a name="record-fields"></a><span data-ttu-id="02a6d-110">Поля записей</span><span class="sxs-lookup"><span data-stu-id="02a6d-110">Record Fields</span></span>

<span data-ttu-id="02a6d-111">Различие различий между гетерогенными данными и однородными данными состоит в том, что для первого, каждой строки данных или **записи**, может быть разный набор столбцов или **полей**.</span><span class="sxs-lookup"><span data-stu-id="02a6d-111">The distinguishing difference between heterogeneous data and homogeneous data is that for the former, each row of data, or **Record**, can have a different set of columns, or **Fields**.</span></span> <span data-ttu-id="02a6d-112">Для однородных данных каждая строка имеет одинаковый набор столбцов.</span><span class="sxs-lookup"><span data-stu-id="02a6d-112">For homogeneous data, each row has the same set of columns.</span></span> <span data-ttu-id="02a6d-113">Дополнительные сведения о полях, относящихся к поставщику публикации в Интернете, можно узнать в разделе [записи и поля, предоставляемЫе поставщиком](records-and-provider-supplied-fields.md).</span><span class="sxs-lookup"><span data-stu-id="02a6d-113">For more information about the fields specific to the Internet Publishing Provider, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>

## <a name="appending-new-fields"></a><span data-ttu-id="02a6d-114">Добавление новых полей</span><span class="sxs-lookup"><span data-stu-id="02a6d-114">Appending New Fields</span></span>

<span data-ttu-id="02a6d-115">Несколько объектов ADO были расширены для работы в сочетании с объектами **Record** и **Stream** .</span><span class="sxs-lookup"><span data-stu-id="02a6d-115">Several ADO objects have been enhanced to work in conjunction with **Record** and **Stream** objects.</span></span>

  - <span data-ttu-id="02a6d-116">Метод [append](append-method-ado.md) коллекции [Fields](fields-collection-ado.md) , который создает и добавляет объект [field](field-object-ado.md) в коллекцию, может также указать значение **поля**.</span><span class="sxs-lookup"><span data-stu-id="02a6d-116">The [Fields](fields-collection-ado.md) collection [Append](append-method-ado.md) method, which creates and adds a [Field](field-object-ado.md) object to the collection, can also specify the value of the **Field**.</span></span>

  - <span data-ttu-id="02a6d-117">Метод [Update](update-method-ado.md) завершает Добавление или удаление полей в коллекции.</span><span class="sxs-lookup"><span data-stu-id="02a6d-117">The [Update](update-method-ado.md) method finalizes the addition or deletion of fields to the collection.</span></span>

  - <span data-ttu-id="02a6d-118">В качестве ярлыка и альтернативы методу **append** вы можете создать поля, просто назначив значение неопределенному или ранее удаленному полю.</span><span class="sxs-lookup"><span data-stu-id="02a6d-118">As a shortcut and alternative to the **Append** method, you may create fields by simply assigning a value to an undefined or previously deleted field.</span></span>

## <a name="see-also"></a><span data-ttu-id="02a6d-119">См. также</span><span class="sxs-lookup"><span data-stu-id="02a6d-119">See also</span></span>

- [<span data-ttu-id="02a6d-120">Разделы сценариев публикации в Интернете</span><span class="sxs-lookup"><span data-stu-id="02a6d-120">Internet Publishing Scenario topics</span></span>](internet-publishing-scenario.md)
