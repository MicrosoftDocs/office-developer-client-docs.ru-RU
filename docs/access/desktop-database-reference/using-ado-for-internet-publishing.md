---
title: Использование ADO для публикации в Интернете
TOCTitle: Using ADO for Internet Publishing
ms:assetid: 1e829783-fc12-e303-6f12-2df1ca96cb0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248975(v=office.15)
ms:contentKeyID: 48543622
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e3a9c6b8dc7a6dc88ac6baf8d05e1baf4a0e048b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868555"
---
# <a name="using-ado-for-internet-publishing"></a><span data-ttu-id="33b17-102">Использование ADO для публикации в Интернете</span><span class="sxs-lookup"><span data-stu-id="33b17-102">Using ADO for Internet Publishing</span></span>


<span data-ttu-id="33b17-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="33b17-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="33b17-104">[Поставщик OLE DB для публикации Интернет](the-ole-db-provider-for-internet-publishing.md) показывает конкретном примере доступа к разнородных данных с помощью ADO.</span><span class="sxs-lookup"><span data-stu-id="33b17-104">[The OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md) shows a specific example of accessing heterogeneous data with ADO.</span></span> <span data-ttu-id="33b17-105">Во время примеров, описанных в этом разделе, относится только к с помощью службу публикации в Интернете, принципы показано должно быть одинаковым при использовании ADO с другими поставщиками для разнородных данных, таких как поставщика в хранилище электронной почты.</span><span class="sxs-lookup"><span data-stu-id="33b17-105">While the examples in this section will be specific to using the Internet Publishing Provider, the principles demonstrated should be similar when using ADO with other providers to heterogeneous data, such as a provider to an e-mail store.</span></span>

## <a name="urls"></a><span data-ttu-id="33b17-106">URL-адреса</span><span class="sxs-lookup"><span data-stu-id="33b17-106">URLs</span></span>

<span data-ttu-id="33b17-107">Указатели универсальный код ресурса (URL-адреса) можно использовать в качестве альтернативы для строки подключения и текст команды для указания источников данных и папки для файлов и папок.</span><span class="sxs-lookup"><span data-stu-id="33b17-107">Uniform Resource Locators (URLs) can be used as an alternative to connection strings and command text to specify data sources and the location of files and directories.</span></span> <span data-ttu-id="33b17-108">URL-адреса, можно использовать с существующими объектами [подключения](connection-object-ado.md) и **записей** , а также с объектами **потока** и **записи** .</span><span class="sxs-lookup"><span data-stu-id="33b17-108">You can use URLs with the existing [Connection](connection-object-ado.md) and **Recordset** objects as well as with the **Record** and **Stream** objects.</span></span>

<span data-ttu-id="33b17-109">Дополнительные сведения об использовании URL-адреса можно [абсолютного и относительных URL-адресов](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="33b17-109">For more information about using URLs, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span>

## <a name="record-fields"></a><span data-ttu-id="33b17-110">Поля записей</span><span class="sxs-lookup"><span data-stu-id="33b17-110">Record Fields</span></span>

<span data-ttu-id="33b17-111">Отличительные различие между разнородных данных и однородных данных, для предыдущих версий, каждой строки данных или **записи**, а может иметь другой набор столбцы или **поля**.</span><span class="sxs-lookup"><span data-stu-id="33b17-111">The distinguishing difference between heterogeneous data and homogeneous data is that for the former, each row of data, or **Record**, can have a different set of columns, or **Fields**.</span></span> <span data-ttu-id="33b17-112">Для однородных данных каждая строка имеет тот же набор столбцов.</span><span class="sxs-lookup"><span data-stu-id="33b17-112">For homogeneous data, each row has the same set of columns.</span></span> <span data-ttu-id="33b17-113">Дополнительные сведения о полях конкретных службу публикации в Интернете можно [записей и полей Provider-Supplied](records-and-provider-supplied-fields.md).</span><span class="sxs-lookup"><span data-stu-id="33b17-113">For more information about the fields specific to the Internet Publishing Provider, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>

## <a name="appending-new-fields"></a><span data-ttu-id="33b17-114">Добавление новых полей</span><span class="sxs-lookup"><span data-stu-id="33b17-114">Appending New Fields</span></span>

<span data-ttu-id="33b17-115">Несколько объектов ADO были улучшены для использования в сочетании с объектами **потока** и **записи** .</span><span class="sxs-lookup"><span data-stu-id="33b17-115">Several ADO objects have been enhanced to work in conjunction with **Record** and **Stream** objects.</span></span>

  - <span data-ttu-id="33b17-116">Коллекции [полей](fields-collection-ado.md) [Добавить](append-method-ado.md) метод, который создает и добавляет в коллекцию объекта [поля](field-object-ado.md) , можно также указать значение **поля**.</span><span class="sxs-lookup"><span data-stu-id="33b17-116">The [Fields](fields-collection-ado.md) collection [Append](append-method-ado.md) method, which creates and adds a [Field](field-object-ado.md) object to the collection, can also specify the value of the **Field**.</span></span>

  - <span data-ttu-id="33b17-117">Метод [Update](update-method-ado.md) завершает добавления или удаления полей в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="33b17-117">The [Update](update-method-ado.md) method finalizes the addition or deletion of fields to the collection.</span></span>

  - <span data-ttu-id="33b17-118">Ярлык и альтернативу метод **Append** можно создать поля, просто значение присваивается значение undefined или ранее удаленного поля.</span><span class="sxs-lookup"><span data-stu-id="33b17-118">As a shortcut and alternative to the **Append** method, you may create fields by simply assigning a value to an undefined or previously deleted field.</span></span>

## <a name="see-also"></a><span data-ttu-id="33b17-119">См. также</span><span class="sxs-lookup"><span data-stu-id="33b17-119">See also</span></span>

- [<span data-ttu-id="33b17-120">Разделы сценарий публикации в Интернете</span><span class="sxs-lookup"><span data-stu-id="33b17-120">Internet Publishing Scenario topics</span></span>](internet-publishing-scenario.md)