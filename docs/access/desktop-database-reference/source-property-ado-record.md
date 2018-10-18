---
title: Source Property (ADO Record)
TOCTitle: Source Property (ADO Record)
ms:assetid: f36f0f5f-4493-d8c5-db4b-c72f5031bcb3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250235(v=office.15)
ms:contentKeyID: 48548670
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d6e010ce8db93baaf8faddaeff5ab4dabda6a84
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603387"
---
# <a name="source-property-ado-record"></a><span data-ttu-id="72e06-102">Source Property (ADO Record)</span><span class="sxs-lookup"><span data-stu-id="72e06-102">Source Property (ADO Record)</span></span>


<span data-ttu-id="72e06-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="72e06-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="72e06-104">Указывает источник данных или объектов, представленных в [записи](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="72e06-104">Indicates the data source or object represented by the [Record](record-object-ado.md).</span></span>

<span data-ttu-id="72e06-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="72e06-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="72e06-106">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="72e06-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="72e06-107">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="72e06-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="72e06-108">master</span><span class="sxs-lookup"><span data-stu-id="72e06-108">master</span></span>

<span data-ttu-id="72e06-109">Задает или возвращает значение **типа Variant** , которое указывает, сущности, представленной **записи**.</span><span class="sxs-lookup"><span data-stu-id="72e06-109">Sets or returns a **Variant** value that indicates the entity represented by the **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="72e06-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="72e06-110">Remarks</span></span>

<span data-ttu-id="72e06-111">Свойство **Source** возвращает *исходный* аргумент методу [Open](open-method-ado-record.md) объекта **записи** .</span><span class="sxs-lookup"><span data-stu-id="72e06-111">The **Source** property returns the *Source* argument of the **Record** object [Open](open-method-ado-record.md) method.</span></span> <span data-ttu-id="72e06-112">Он может содержать абсолютное или относительное строку URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="72e06-112">It can contain an absolute or relative URL string.</span></span> <span data-ttu-id="72e06-113">Абсолютный URL-адрес может использоваться без установки свойства [ActiveConnection](activeconnection-property-ado.md) непосредственно открыть объект **записи** .</span><span class="sxs-lookup"><span data-stu-id="72e06-113">An absolute URL can be used without setting the [ActiveConnection](activeconnection-property-ado.md) property to directly open the **Record** object.</span></span> <span data-ttu-id="72e06-114">В этом случае создается объект **подключения** неявных.</span><span class="sxs-lookup"><span data-stu-id="72e06-114">An implicit **Connection** object is created in this case.</span></span>

<span data-ttu-id="72e06-115">Свойство **Source** также может содержать ссылки на уже открытой **записей**, открывающий **записи** объект, представляющий текущую строку в **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="72e06-115">The **Source** property can also contain a reference to an already open **Recordset**, which opens a **Record** object representing the current row in the **Recordset**.</span></span>

<span data-ttu-id="72e06-116">Свойство **Source** может также содержать ссылку на объект [команды](command-object-ado.md) , который возвращает одну строку данных от поставщика.</span><span class="sxs-lookup"><span data-stu-id="72e06-116">The **Source** property could also contain a reference to a [Command](command-object-ado.md) object which returns a single row of data from the provider.</span></span>

<span data-ttu-id="72e06-117">Если задано свойство **ActiveConnection** , свойство **Source** должен указывать некоторые объект, который существует в пределах это подключение.</span><span class="sxs-lookup"><span data-stu-id="72e06-117">If the **ActiveConnection** property is also set, then the **Source** property must point to some object that exists within the scope of that connection.</span></span> <span data-ttu-id="72e06-118">Например в пространствах имен структура дерева, если свойство **Source** содержит абсолютный URL-адрес оно должно указывать на узел, который существует внутри области узла, определяемую средством URL-адрес в строку подключения.</span><span class="sxs-lookup"><span data-stu-id="72e06-118">For example, in tree-structured namespaces, if the **Source** property contains an absolute URL, it must point to a node that exists inside the scope of the node identified by the URL in the connection string.</span></span> <span data-ttu-id="72e06-119">Если свойство **Source** содержит относительный URL-адрес, он проверяется в контексте, заданной свойством **ActiveConnection** .</span><span class="sxs-lookup"><span data-stu-id="72e06-119">If the **Source** property contains a relative URL, then it is validated within the context set by the **ActiveConnection** property.</span></span>

<span data-ttu-id="72e06-120">Свойство **Source** — чтение и запись во время объект **записи** закрывается и доступен только для чтения, когда объект **записи** открыт.</span><span class="sxs-lookup"><span data-stu-id="72e06-120">The **Source** property is read/write while the **Record** object is closed, and is read-only while the **Record** object is open.</span></span>

<span data-ttu-id="72e06-121"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="72e06-121"><<<<<<< HEAD</span></span>

> [!NOTE]
> <P><span data-ttu-id="72e06-122">URL-адреса, с помощью схемы http автоматически вызывает <A href="microsoft-ole-db-provider-for-internet-publishing.md">Поставщик Microsoft OLE DB для публикации Интернет</A>.</span><span class="sxs-lookup"><span data-stu-id="72e06-122">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>.</span></span> <span data-ttu-id="72e06-123">Для получения дополнительных сведений см <A href="absolute-and-relative-urls.md">абсолютного и относительных URL-адресов</A>.</span><span class="sxs-lookup"><span data-stu-id="72e06-123">For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>
=======
> [!NOTE]
> <span data-ttu-id="72e06-124">URL-адреса, с помощью схемы http автоматически вызывает [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="72e06-124">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="72e06-125">Для получения дополнительных сведений см [абсолютных и относительных URL-адресов](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="72e06-125">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>
>>>>>>> <span data-ttu-id="72e06-126">master</span><span class="sxs-lookup"><span data-stu-id="72e06-126">master</span></span>


