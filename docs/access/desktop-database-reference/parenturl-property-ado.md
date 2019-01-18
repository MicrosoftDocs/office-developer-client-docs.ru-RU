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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707817"
---
# <a name="parenturl-property-ado"></a><span data-ttu-id="1db72-102">Свойство ParentURL (ADO)</span><span class="sxs-lookup"><span data-stu-id="1db72-102">ParentURL property (ADO)</span></span>

<span data-ttu-id="1db72-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1db72-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1db72-104">Указывает строку абсолютный URL-адрес, указывающий на родительской [записи](record-object-ado.md) текущего объекта **записи** .</span><span class="sxs-lookup"><span data-stu-id="1db72-104">Indicates an absolute URL string that points to the parent [Record](record-object-ado.md) of the current **Record** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="1db72-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1db72-105">Return value</span></span>

<span data-ttu-id="1db72-106">Возвращает **строковое** значение, которое указывает URL-адрес родительской **записи**.</span><span class="sxs-lookup"><span data-stu-id="1db72-106">Returns a **String** value that indicates the URL of the parent **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1db72-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="1db72-107">Remarks</span></span>

<span data-ttu-id="1db72-108">Свойство **ParentURL** зависит от источника, используемого для открытия объект **записи** .</span><span class="sxs-lookup"><span data-stu-id="1db72-108">The **ParentURL** property depends upon the source used to open the **Record** object.</span></span> <span data-ttu-id="1db72-109">Например, **записи** можно открыть с источником, содержащий относительный путь каталог, указанный в свойстве [ActiveConnection](activeconnection-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1db72-109">For example, the **Record** may be opened with a source containing a relative path name of a directory referenced by the [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

<span data-ttu-id="1db72-110">Предположим, что «second» папки содержится в разделе «первый».</span><span class="sxs-lookup"><span data-stu-id="1db72-110">Suppose "second" is a folder contained under "first".</span></span> <span data-ttu-id="1db72-111">Откройте объект **записи** со следующими:</span><span class="sxs-lookup"><span data-stu-id="1db72-111">Open the **Record** object with the following:</span></span>

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

<span data-ttu-id="1db72-112">Сейчас, — это значение свойства **ParentURL** **ParentURL** свойством является "https://first", то же, что **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="1db72-112">Now, the value of the **ParentURL** property is **ParentURL** property is "https://first" , the same as **ActiveConnection**.</span></span>

<span data-ttu-id="1db72-113">Источник также могут быть абсолютный URL-адрес например, "https://first/second".</span><span class="sxs-lookup"><span data-stu-id="1db72-113">The source may also be an absolute URL such as, "https://first/second" .</span></span> <span data-ttu-id="1db72-114">Является ли данное свойство **ParentURL** нажмите "https://first", уровень выше.</span><span class="sxs-lookup"><span data-stu-id="1db72-114">The **ParentURL** property is then "https://first" , the level above .</span></span> <span data-ttu-id="1db72-115">Является ли данное свойство **ParentURL** нажмите "https://first", уровень выше «секунды».</span><span class="sxs-lookup"><span data-stu-id="1db72-115">The **ParentURL** property is then "https://first" , the level above "second" .</span></span>

<span data-ttu-id="1db72-116">Это свойство может иметь значение null, если:</span><span class="sxs-lookup"><span data-stu-id="1db72-116">This property may be a null value if:</span></span>

- <span data-ttu-id="1db72-117">Родительского объекта нет текущего объекта; Например, если объект **записи** представляет корневой каталог.</span><span class="sxs-lookup"><span data-stu-id="1db72-117">There is no parent for the current object; for example, if the **Record** object represents the root of a directory.</span></span>

- <span data-ttu-id="1db72-118">Объект **записи** представляет сущности, которая не может быть указан URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="1db72-118">The **Record** object represents an entity that cannot be specified with a URL.</span></span>

<span data-ttu-id="1db72-119">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1db72-119">This property is read-only.</span></span>


> [!NOTE]
> - <span data-ttu-id="1db72-120">Это свойство поддерживается только с поставщиками исходного документа, такими как [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="1db72-120">This property is only supported by document source providers, such as the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="1db72-121">Для получения дополнительных сведений см [записей и Provider-Supplied полей](records-and-provider-supplied-fields.md).</span><span class="sxs-lookup"><span data-stu-id="1db72-121">For more information, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>
> - <span data-ttu-id="1db72-122">URL-адреса, с помощью схемы http автоматически вызывает поставщик Microsoft OLE DB для публикации Интернет.</span><span class="sxs-lookup"><span data-stu-id="1db72-122">URLs using the http scheme will automatically invoke the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="1db72-123">Для получения дополнительных сведений см [абсолютного и относительных URL-адресов](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="1db72-123">For more information, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span> 
> - <span data-ttu-id="1db72-124">Если текущая запись содержит записи данных из набора **записей**ADO, доступ к свойству **ParentURL** вызывает ошибку времени выполнения, указывающего на то, что URL-адрес не является возможных.</span><span class="sxs-lookup"><span data-stu-id="1db72-124">If the current record contains a data record from an ADO **Recordset**, accessing the **ParentURL** property causes a run-time error, indicating that no URL is possible.</span></span>


