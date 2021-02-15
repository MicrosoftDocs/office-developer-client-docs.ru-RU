---
title: Свойство Source (объект Record в ADO)
TOCTitle: Source property (ADO Record)
ms:assetid: f36f0f5f-4493-d8c5-db4b-c72f5031bcb3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250235(v=office.15)
ms:contentKeyID: 48548670
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9bd1e1259eb7b089d0387dd385ee5157eeac2f34
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314555"
---
# <a name="source-property-ado-record"></a><span data-ttu-id="327fb-102">Свойство Source (объект Record в ADO)</span><span class="sxs-lookup"><span data-stu-id="327fb-102">Source property (ADO Record)</span></span>


<span data-ttu-id="327fb-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="327fb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="327fb-104">Указывает источник данных или объект, представленный [записью.](record-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="327fb-104">Indicates the data source or object represented by the [Record](record-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="327fb-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="327fb-105">Settings and return values</span></span>

<span data-ttu-id="327fb-106">Задает или возвращает значение **Variant,** которое указывает сущность, представленную **записью.**</span><span class="sxs-lookup"><span data-stu-id="327fb-106">Sets or returns a **Variant** value that indicates the entity represented by the **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="327fb-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="327fb-107">Remarks</span></span>

<span data-ttu-id="327fb-108">Свойство **Source** возвращает аргумент *Source* метода Open объекта **Record.** [](open-method-ado-record.md)</span><span class="sxs-lookup"><span data-stu-id="327fb-108">The **Source** property returns the *Source* argument of the **Record** object [Open](open-method-ado-record.md) method.</span></span> <span data-ttu-id="327fb-109">Он может содержать абсолютную или относительную строку URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="327fb-109">It can contain an absolute or relative URL string.</span></span> <span data-ttu-id="327fb-110">Абсолютный URL-адрес можно использовать без настройки свойства [ActiveConnection](activeconnection-property-ado.md) для непосредственного открытия **объекта Record.**</span><span class="sxs-lookup"><span data-stu-id="327fb-110">An absolute URL can be used without setting the [ActiveConnection](activeconnection-property-ado.md) property to directly open the **Record** object.</span></span> <span data-ttu-id="327fb-111">В этом **случае** создается неявный объект Connection.</span><span class="sxs-lookup"><span data-stu-id="327fb-111">An implicit **Connection** object is created in this case.</span></span>

<span data-ttu-id="327fb-112">Свойство **Source** также может содержать ссылку на уже открытый набор записей, который открывает объект **Record,** представляющий текущую строку в **наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="327fb-112">The **Source** property can also contain a reference to an already open **Recordset**, which opens a **Record** object representing the current row in the **Recordset**.</span></span>

<span data-ttu-id="327fb-113">Свойство **Source** также может содержать ссылку на объект [Command,](command-object-ado.md) который возвращает одну строку данных от поставщика.</span><span class="sxs-lookup"><span data-stu-id="327fb-113">The **Source** property could also contain a reference to a [Command](command-object-ado.md) object which returns a single row of data from the provider.</span></span>

<span data-ttu-id="327fb-114">Если также установлено свойство **ActiveConnection,** свойство **Source** должно указать на какой-либо объект, который существует в области этого подключения.</span><span class="sxs-lookup"><span data-stu-id="327fb-114">If the **ActiveConnection** property is also set, then the **Source** property must point to some object that exists within the scope of that connection.</span></span> <span data-ttu-id="327fb-115">Например, в древоструктуренных пространствах имен, если свойство **Source** содержит абсолютный URL-адрес, оно должно указать узел, который существует в области узла, задаемого URL-адресом в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="327fb-115">For example, in tree-structured namespaces, if the **Source** property contains an absolute URL, it must point to a node that exists inside the scope of the node identified by the URL in the connection string.</span></span> <span data-ttu-id="327fb-116">Если свойство **Source** содержит относительный URL-адрес, оно проверяется в контексте, задаемом **свойством ActiveConnection.**</span><span class="sxs-lookup"><span data-stu-id="327fb-116">If the **Source** property contains a relative URL, then it is validated within the context set by the **ActiveConnection** property.</span></span>

<span data-ttu-id="327fb-117">Свойство **Source** находится в режиме чтения и записи при закрытии объекта **Record,** а объект **Record** открыт только для чтения.</span><span class="sxs-lookup"><span data-stu-id="327fb-117">The **Source** property is read/write while the **Record** object is closed, and is read-only while the **Record** object is open.</span></span>

> [!NOTE]
> <span data-ttu-id="327fb-118">URL-адреса, использующие схему HTTP, автоматически вызывают поставщика [Microsoft OLE DB для интернет-публикации.](microsoft-ole-db-provider-for-internet-publishing.md)</span><span class="sxs-lookup"><span data-stu-id="327fb-118">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="327fb-119">Дополнительные сведения см. в [сведениях об абсолютных и относительных URL-адресах.](absolute-and-relative-urls.md)</span><span class="sxs-lookup"><span data-stu-id="327fb-119">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


