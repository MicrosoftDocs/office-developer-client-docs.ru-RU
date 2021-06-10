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
# <a name="parenturl-property-ado"></a><span data-ttu-id="2368d-102">Свойство ParentURL (ADO)</span><span class="sxs-lookup"><span data-stu-id="2368d-102">ParentURL property (ADO)</span></span>

<span data-ttu-id="2368d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2368d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2368d-104">Указывает абсолютную строку URL-адреса, которая указывает на родительную [запись](record-object-ado.md) текущего объекта **Record.**</span><span class="sxs-lookup"><span data-stu-id="2368d-104">Indicates an absolute URL string that points to the parent [Record](record-object-ado.md) of the current **Record** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="2368d-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2368d-105">Return value</span></span>

<span data-ttu-id="2368d-106">Возвращает значение **String,** которое указывает URL-адрес родительской **записи.**</span><span class="sxs-lookup"><span data-stu-id="2368d-106">Returns a **String** value that indicates the URL of the parent **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2368d-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="2368d-107">Remarks</span></span>

<span data-ttu-id="2368d-108">Свойство **ParentURL** зависит от источника, используемого для открытия **объекта Record.**</span><span class="sxs-lookup"><span data-stu-id="2368d-108">The **ParentURL** property depends upon the source used to open the **Record** object.</span></span> <span data-ttu-id="2368d-109">Например, **запись может** быть открыта с источником, содержащим относительное имя пути каталога, ссылаясь на [свойство ActiveConnection.](activeconnection-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="2368d-109">For example, the **Record** may be opened with a source containing a relative path name of a directory referenced by the [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

<span data-ttu-id="2368d-110">Предположим, что "second" — это папка, содержаная под "первым".</span><span class="sxs-lookup"><span data-stu-id="2368d-110">Suppose "second" is a folder contained under "first".</span></span> <span data-ttu-id="2368d-111">Откройте объект **Record** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2368d-111">Open the **Record** object with the following:</span></span>

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

<span data-ttu-id="2368d-112">Теперь значение свойства **ParentURL** — свойство **ParentURL** — ", то же самое, что https://first и **ActiveConnection.**</span><span class="sxs-lookup"><span data-stu-id="2368d-112">Now, the value of the **ParentURL** property is **ParentURL** property is "https://first" , the same as **ActiveConnection**.</span></span>

<span data-ttu-id="2368d-113">Источником также может быть абсолютный URL-адрес, например " https://first/second .</span><span class="sxs-lookup"><span data-stu-id="2368d-113">The source may also be an absolute URL such as, "https://first/second" .</span></span> <span data-ttu-id="2368d-114">Свойство **ParentURL** — это https://first ", уровень выше .</span><span class="sxs-lookup"><span data-stu-id="2368d-114">The **ParentURL** property is then "https://first" , the level above .</span></span> <span data-ttu-id="2368d-115">Свойство **ParentURL** — это https://first ", уровень выше "second".</span><span class="sxs-lookup"><span data-stu-id="2368d-115">The **ParentURL** property is then "https://first" , the level above "second" .</span></span>

<span data-ttu-id="2368d-116">Это свойство может быть значением null, если:</span><span class="sxs-lookup"><span data-stu-id="2368d-116">This property may be a null value if:</span></span>

- <span data-ttu-id="2368d-117">Для текущего объекта не существует родительского родителя; например, если **объект Record** представляет корень каталога.</span><span class="sxs-lookup"><span data-stu-id="2368d-117">There is no parent for the current object; for example, if the **Record** object represents the root of a directory.</span></span>

- <span data-ttu-id="2368d-118">Объект **Record** представляет объект, который не может быть указан с URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="2368d-118">The **Record** object represents an entity that cannot be specified with a URL.</span></span>

<span data-ttu-id="2368d-119">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2368d-119">This property is read-only.</span></span>


> [!NOTE]
> - <span data-ttu-id="2368d-120">Это свойство поддерживается только поставщиками источников документов, такими как [поставщик DB Microsoft OLE для публикации в Интернете.](microsoft-ole-db-provider-for-internet-publishing.md)</span><span class="sxs-lookup"><span data-stu-id="2368d-120">This property is only supported by document source providers, such as the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="2368d-121">Дополнительные сведения см. в [Provider-Supplied Records and Provider-Supplied Fields.](records-and-provider-supplied-fields.md)</span><span class="sxs-lookup"><span data-stu-id="2368d-121">For more information, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>
> - <span data-ttu-id="2368d-122">URL-адреса, использующие схему http, автоматически вызывают поставщика DB Microsoft OLE для публикации в Интернете.</span><span class="sxs-lookup"><span data-stu-id="2368d-122">URLs using the http scheme will automatically invoke the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="2368d-123">Дополнительные сведения см. в [url-адресах Absolute и Relative.](absolute-and-relative-urls.md)</span><span class="sxs-lookup"><span data-stu-id="2368d-123">For more information, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span> 
> - <span data-ttu-id="2368d-124">Если текущая запись содержит запись данных из ADO **Recordset,** доступ к свойству **ParentURL** вызывает ошибку во время запуска, что указывает на невозможность URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="2368d-124">If the current record contains a data record from an ADO **Recordset**, accessing the **ParentURL** property causes a run-time error, indicating that no URL is possible.</span></span>


