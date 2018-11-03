---
title: Свойство Source (объект Record в ADO)
TOCTitle: Source property (ADO Record)
ms:assetid: f36f0f5f-4493-d8c5-db4b-c72f5031bcb3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250235(v=office.15)
ms:contentKeyID: 48548670
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b41521ac3b4ba0f07eac188a7103025be2800e4d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946505"
---
# <a name="source-property-ado-record"></a><span data-ttu-id="56488-102">Свойство Source (объект Record в ADO)</span><span class="sxs-lookup"><span data-stu-id="56488-102">Source property (ADO Record)</span></span>


<span data-ttu-id="56488-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="56488-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="56488-104">Указывает источник данных или объектов, представленных в [записи](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="56488-104">Indicates the data source or object represented by the [Record](record-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="56488-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="56488-105">Settings and return values</span></span>

<span data-ttu-id="56488-106">Задает или возвращает значение **типа Variant** , которое указывает, сущности, представленной **записи**.</span><span class="sxs-lookup"><span data-stu-id="56488-106">Sets or returns a **Variant** value that indicates the entity represented by the **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="56488-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="56488-107">Remarks</span></span>

<span data-ttu-id="56488-108">Свойство **Source** возвращает *исходный* аргумент методу [Open](open-method-ado-record.md) объекта **записи** .</span><span class="sxs-lookup"><span data-stu-id="56488-108">The **Source** property returns the *Source* argument of the **Record** object [Open](open-method-ado-record.md) method.</span></span> <span data-ttu-id="56488-109">Он может содержать абсолютное или относительное строку URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="56488-109">It can contain an absolute or relative URL string.</span></span> <span data-ttu-id="56488-110">Абсолютный URL-адрес может использоваться без установки свойства [ActiveConnection](activeconnection-property-ado.md) непосредственно открыть объект **записи** .</span><span class="sxs-lookup"><span data-stu-id="56488-110">An absolute URL can be used without setting the [ActiveConnection](activeconnection-property-ado.md) property to directly open the **Record** object.</span></span> <span data-ttu-id="56488-111">В этом случае создается объект **подключения** неявных.</span><span class="sxs-lookup"><span data-stu-id="56488-111">An implicit **Connection** object is created in this case.</span></span>

<span data-ttu-id="56488-112">Свойство **Source** также может содержать ссылки на уже открытой **записей**, открывающий **записи** объект, представляющий текущую строку в **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="56488-112">The **Source** property can also contain a reference to an already open **Recordset**, which opens a **Record** object representing the current row in the **Recordset**.</span></span>

<span data-ttu-id="56488-113">Свойство **Source** может также содержать ссылку на объект [команды](command-object-ado.md) , который возвращает одну строку данных от поставщика.</span><span class="sxs-lookup"><span data-stu-id="56488-113">The **Source** property could also contain a reference to a [Command](command-object-ado.md) object which returns a single row of data from the provider.</span></span>

<span data-ttu-id="56488-114">Если задано свойство **ActiveConnection** , свойство **Source** должен указывать некоторые объект, который существует в пределах это подключение.</span><span class="sxs-lookup"><span data-stu-id="56488-114">If the **ActiveConnection** property is also set, then the **Source** property must point to some object that exists within the scope of that connection.</span></span> <span data-ttu-id="56488-115">Например в пространствах имен структура дерева, если свойство **Source** содержит абсолютный URL-адрес оно должно указывать на узел, который существует внутри области узла, определяемую средством URL-адрес в строку подключения.</span><span class="sxs-lookup"><span data-stu-id="56488-115">For example, in tree-structured namespaces, if the **Source** property contains an absolute URL, it must point to a node that exists inside the scope of the node identified by the URL in the connection string.</span></span> <span data-ttu-id="56488-116">Если свойство **Source** содержит относительный URL-адрес, он проверяется в контексте, заданной свойством **ActiveConnection** .</span><span class="sxs-lookup"><span data-stu-id="56488-116">If the **Source** property contains a relative URL, then it is validated within the context set by the **ActiveConnection** property.</span></span>

<span data-ttu-id="56488-117">Свойство **Source** — чтение и запись во время объект **записи** закрывается и доступен только для чтения, когда объект **записи** открыт.</span><span class="sxs-lookup"><span data-stu-id="56488-117">The **Source** property is read/write while the **Record** object is closed, and is read-only while the **Record** object is open.</span></span>

> [!NOTE]
> <span data-ttu-id="56488-118">URL-адреса, с помощью схемы http автоматически вызывает [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="56488-118">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="56488-119">Для получения дополнительных сведений см [абсолютных и относительных URL-адресов](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="56488-119">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


