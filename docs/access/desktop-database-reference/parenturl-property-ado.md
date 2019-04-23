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
# <a name="parenturl-property-ado"></a><span data-ttu-id="9cfad-102">Свойство ParentURL (ADO)</span><span class="sxs-lookup"><span data-stu-id="9cfad-102">ParentURL property (ADO)</span></span>

<span data-ttu-id="9cfad-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9cfad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9cfad-104">Указывает строку абсолютного URL-адреса, указывающую на родительскую [запись](record-object-ado.md) текущего объекта **Record** .</span><span class="sxs-lookup"><span data-stu-id="9cfad-104">Indicates an absolute URL string that points to the parent [Record](record-object-ado.md) of the current **Record** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="9cfad-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9cfad-105">Return value</span></span>

<span data-ttu-id="9cfad-106">Возвращает **строковое** значение, УКАЗЫВАЮЩЕЕ URL-адрес родительской **записи**.</span><span class="sxs-lookup"><span data-stu-id="9cfad-106">Returns a **String** value that indicates the URL of the parent **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cfad-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="9cfad-107">Remarks</span></span>

<span data-ttu-id="9cfad-108">Свойство **ParentURL** зависит от источника, используемого для открытия объекта **Record** .</span><span class="sxs-lookup"><span data-stu-id="9cfad-108">The **ParentURL** property depends upon the source used to open the **Record** object.</span></span> <span data-ttu-id="9cfad-109">Например, **запись** может быть открыта с источником, содержащим относительный путь к каталогу, на который ссылается свойство [ActiveConnection](activeconnection-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="9cfad-109">For example, the **Record** may be opened with a source containing a relative path name of a directory referenced by the [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

<span data-ttu-id="9cfad-110">Предположим, что "Second" — это папка, которая находится в разделе "First".</span><span class="sxs-lookup"><span data-stu-id="9cfad-110">Suppose "second" is a folder contained under "first".</span></span> <span data-ttu-id="9cfad-111">Откройте объект **Record** , выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="9cfad-111">Open the **Record** object with the following:</span></span>

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

<span data-ttu-id="9cfad-112">Теперь значение свойства **ParentURL** равно **ParentURL** свойству "https://first", то же, что и **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="9cfad-112">Now, the value of the **ParentURL** property is **ParentURL** property is "https://first" , the same as **ActiveConnection**.</span></span>

<span data-ttu-id="9cfad-113">Источник также может быть абсолютным URL-АДРЕСом, напримерhttps://first/second, "".</span><span class="sxs-lookup"><span data-stu-id="9cfad-113">The source may also be an absolute URL such as, "https://first/second" .</span></span> <span data-ttu-id="9cfad-114">В качестве значения свойства **ParentURL** используетсяhttps://firstуровень выше.</span><span class="sxs-lookup"><span data-stu-id="9cfad-114">The **ParentURL** property is then "https://first" , the level above .</span></span> <span data-ttu-id="9cfad-115">В качестве значения свойства **ParentURL** используетсяhttps://firstуровень выше "второй".</span><span class="sxs-lookup"><span data-stu-id="9cfad-115">The **ParentURL** property is then "https://first" , the level above "second" .</span></span>

<span data-ttu-id="9cfad-116">Это свойство может иметь значение null, если:</span><span class="sxs-lookup"><span data-stu-id="9cfad-116">This property may be a null value if:</span></span>

- <span data-ttu-id="9cfad-117">Родительский объект для текущего объекта отсутствует; Например, если объект **Record** представляет корень каталога.</span><span class="sxs-lookup"><span data-stu-id="9cfad-117">There is no parent for the current object; for example, if the **Record** object represents the root of a directory.</span></span>

- <span data-ttu-id="9cfad-118">Объект **Record** представляет сущность, которая не может быть указана с URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="9cfad-118">The **Record** object represents an entity that cannot be specified with a URL.</span></span>

<span data-ttu-id="9cfad-119">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9cfad-119">This property is read-only.</span></span>


> [!NOTE]
> - <span data-ttu-id="9cfad-120">Это свойство поддерживается только поставщиками источника документов, такими как [поставщик Microsoft OLE DB для публикации в Интернете](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="9cfad-120">This property is only supported by document source providers, such as the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="9cfad-121">Для получения дополнительных сведений см [записи и поля, предоставляемЫе поставщиком](records-and-provider-supplied-fields.md).</span><span class="sxs-lookup"><span data-stu-id="9cfad-121">For more information, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>
> - <span data-ttu-id="9cfad-122">URL-адреса, использующие схему HTTP, автоматически будут вызывать поставщик Microsoft OLE DB для публикации в Интернете.</span><span class="sxs-lookup"><span data-stu-id="9cfad-122">URLs using the http scheme will automatically invoke the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="9cfad-123">Для получения дополнительных сведений см [абсолютные и ОтносительНые URL-адреса](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="9cfad-123">For more information, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span> 
> - <span data-ttu-id="9cfad-124">Если текущая запись содержит запись данных из **набора записей**ADO, то при доступе к свойству **ParentURL** возникает ошибка времени выполнения, указывающая на то, что URL-адрес невозможен.</span><span class="sxs-lookup"><span data-stu-id="9cfad-124">If the current record contains a data record from an ADO **Recordset**, accessing the **ParentURL** property causes a run-time error, indicating that no URL is possible.</span></span>


