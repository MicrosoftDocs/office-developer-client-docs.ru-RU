---
title: Свойство ParentURL (ADO)
TOCTitle: ParentURL property (ADO)
ms:assetid: ec7ec476-6f9e-8486-fe02-74995975df5c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15)
ms:contentKeyID: 48548517
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8e3735147f813d904c206910ff319913f056946e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287719"
---
# <a name="parenturl-property-ado"></a><span data-ttu-id="976e8-102">Свойство ParentURL (ADO)</span><span class="sxs-lookup"><span data-stu-id="976e8-102">ParentURL property (ADO)</span></span>

<span data-ttu-id="976e8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="976e8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="976e8-104">Указывает абсолютную строку URL-адреса, которая указывает на родительская [запись](record-object-ado.md) текущего объекта **Record.**</span><span class="sxs-lookup"><span data-stu-id="976e8-104">Indicates an absolute URL string that points to the parent [Record](record-object-ado.md) of the current **Record** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="976e8-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="976e8-105">Return value</span></span>

<span data-ttu-id="976e8-106">Возвращает **строку,** которая указывает URL-адрес родительской **записи.**</span><span class="sxs-lookup"><span data-stu-id="976e8-106">Returns a **String** value that indicates the URL of the parent **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="976e8-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="976e8-107">Remarks</span></span>

<span data-ttu-id="976e8-108">Свойство **ParentURL** зависит от источника, используемого для открытия **объекта Record.**</span><span class="sxs-lookup"><span data-stu-id="976e8-108">The **ParentURL** property depends upon the source used to open the **Record** object.</span></span> <span data-ttu-id="976e8-109">Например, запись **может** быть открыта с источником, содержащим относительный путь к каталогу, на который ссылается свойство [ActiveConnection.](activeconnection-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="976e8-109">For example, the **Record** may be opened with a source containing a relative path name of a directory referenced by the [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

<span data-ttu-id="976e8-110">Предположим, что "second" — это папка, вложенная в папку "first".</span><span class="sxs-lookup"><span data-stu-id="976e8-110">Suppose "second" is a folder contained under "first".</span></span> <span data-ttu-id="976e8-111">Откройте объект **Record** со следующими объектами:</span><span class="sxs-lookup"><span data-stu-id="976e8-111">Open the **Record** object with the following:</span></span>

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

<span data-ttu-id="976e8-112">Теперь свойство **ParentURL** имеет значение **ParentURL** ", то же самое, что https://first и **ActiveConnection.**</span><span class="sxs-lookup"><span data-stu-id="976e8-112">Now, the value of the **ParentURL** property is **ParentURL** property is "https://first" , the same as **ActiveConnection**.</span></span>

<span data-ttu-id="976e8-113">Источником также может быть абсолютный URL-адрес, например " https://first/second .</span><span class="sxs-lookup"><span data-stu-id="976e8-113">The source may also be an absolute URL such as, "https://first/second" .</span></span> <span data-ttu-id="976e8-114">The **ParentURL** property is then https://first " , the level above .</span><span class="sxs-lookup"><span data-stu-id="976e8-114">The **ParentURL** property is then "https://first" , the level above .</span></span> <span data-ttu-id="976e8-115">The **ParentURL** property is then https://first " , the level above "second" .</span><span class="sxs-lookup"><span data-stu-id="976e8-115">The **ParentURL** property is then "https://first" , the level above "second" .</span></span>

<span data-ttu-id="976e8-116">Это свойство может иметь значение NULL, если:</span><span class="sxs-lookup"><span data-stu-id="976e8-116">This property may be a null value if:</span></span>

- <span data-ttu-id="976e8-117">Для текущего объекта не существует родительского объекта; например, если **объект Record** представляет корневой каталог.</span><span class="sxs-lookup"><span data-stu-id="976e8-117">There is no parent for the current object; for example, if the **Record** object represents the root of a directory.</span></span>

- <span data-ttu-id="976e8-118">Объект **Record** представляет сущность, которую нельзя у указывает с помощью URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="976e8-118">The **Record** object represents an entity that cannot be specified with a URL.</span></span>

<span data-ttu-id="976e8-119">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="976e8-119">This property is read-only.</span></span>


> [!NOTE]
> - <span data-ttu-id="976e8-120">Это свойство поддерживается только поставщиками источников документов, такими как [поставщик Microsoft OLE DB для публикации в Интернете.](microsoft-ole-db-provider-for-internet-publishing.md)</span><span class="sxs-lookup"><span data-stu-id="976e8-120">This property is only supported by document source providers, such as the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="976e8-121">Дополнительные сведения [см. в записях и Provider-Supplied полях.](records-and-provider-supplied-fields.md)</span><span class="sxs-lookup"><span data-stu-id="976e8-121">For more information, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>
> - <span data-ttu-id="976e8-122">URL-адреса, использующие схему HTTP, автоматически вызывают поставщика Microsoft OLE DB для интернет-публикации.</span><span class="sxs-lookup"><span data-stu-id="976e8-122">URLs using the http scheme will automatically invoke the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="976e8-123">Дополнительные сведения см. в сведениях [об абсолютных и относительных URL-адресах.](absolute-and-relative-urls.md)</span><span class="sxs-lookup"><span data-stu-id="976e8-123">For more information, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span> 
> - <span data-ttu-id="976e8-124">Если текущая запись содержит запись данных из объекта ADO **Recordset,** доступ к свойству **ParentURL** приводит к ошибке во время запуска, указывающей на то, что URL-адрес невозможен.</span><span class="sxs-lookup"><span data-stu-id="976e8-124">If the current record contains a data record from an ADO **Recordset**, accessing the **ParentURL** property causes a run-time error, indicating that no URL is possible.</span></span>


