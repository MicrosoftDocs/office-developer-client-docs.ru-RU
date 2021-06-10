---
title: Пространства имен (ссылка на настольные базы данных)
TOCTitle: Namespaces
ms:assetid: e39f003c-3d16-1fae-48c5-304593c41f2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250158(v=office.15)
ms:contentKeyID: 48548318
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 905edba502fcc2994be6f6b8e50a7200b66a82b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288627"
---
# <a name="namespaces"></a><span data-ttu-id="88bda-102">Пространства имен</span><span class="sxs-lookup"><span data-stu-id="88bda-102">Namespaces</span></span>

<span data-ttu-id="88bda-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="88bda-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="88bda-104">Формат Сохраняемости XML в ADO использует следующие четыре пространства имен.</span><span class="sxs-lookup"><span data-stu-id="88bda-104">The XML persistence format in ADO uses the following four namespaces.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="88bda-105">Prefix</span><span class="sxs-lookup"><span data-stu-id="88bda-105">Prefix</span></span></p></th>
<th><p><span data-ttu-id="88bda-106">Description</span><span class="sxs-lookup"><span data-stu-id="88bda-106">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88bda-107">s</span><span class="sxs-lookup"><span data-stu-id="88bda-107">s</span></span></p></td>
<td><p><span data-ttu-id="88bda-108">Ссылается на пространство имен XML-Data, содержащее элементы и атрибуты, определяющие схему &quot; &quot; текущего <strong>наборов записей.</strong></span><span class="sxs-lookup"><span data-stu-id="88bda-108">Refers to the &quot;XML-Data&quot; namespace containing the elements and attributes that define the schema of the current <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88bda-109">dt</span><span class="sxs-lookup"><span data-stu-id="88bda-109">dt</span></span></p></td>
<td><p><span data-ttu-id="88bda-110">Ссылается на спецификацию определений типов данных.</span><span class="sxs-lookup"><span data-stu-id="88bda-110">Refers to the data type definitions specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88bda-111">rs</span><span class="sxs-lookup"><span data-stu-id="88bda-111">rs</span></span></p></td>
<td><p><span data-ttu-id="88bda-112">Относится к пространству имен, содержащим элементы и атрибуты, определенные свойствам и атрибутам ADO <strong>Recordset.</strong></span><span class="sxs-lookup"><span data-stu-id="88bda-112">Refers to the namespace containing elements and attributes specific to ADO <strong>Recordset</strong> properties and attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88bda-113">z</span><span class="sxs-lookup"><span data-stu-id="88bda-113">z</span></span></p></td>
<td><p><span data-ttu-id="88bda-114">Ссылается на схему текущего ряда.</span><span class="sxs-lookup"><span data-stu-id="88bda-114">Refers to the schema of the current rowset.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="88bda-115">Клиент не должен добавлять свои теги в эти пространства имен, как это определено спецификацией.</span><span class="sxs-lookup"><span data-stu-id="88bda-115">A client should not add its own tags to these namespaces, as defined by the specification.</span></span> <span data-ttu-id="88bda-116">Например, клиент не должен определять пространство имен как "urn:schemas-microsoft-com:rowset", а затем записывать что-то вроде "rs:MyOwnTag".</span><span class="sxs-lookup"><span data-stu-id="88bda-116">For example, a client should not define a namespace as "urn:schemas-microsoft-com:rowset" and then write out something such as "rs:MyOwnTag."</span></span> <span data-ttu-id="88bda-117">Дополнительные новости о пространствах имен см. в [xML-пространствах имен.](https://www.w3.org/tr/xml-names/)</span><span class="sxs-lookup"><span data-stu-id="88bda-117">To learn more about namespaces, see [XML Namespaces](https://www.w3.org/tr/xml-names/).</span></span>

> [!NOTE]
> <span data-ttu-id="88bda-118">ID для тега схемы должен быть "RowsetSchema", а пространство имен, используемого для ссылки на схему текущего ряда, должно указать на "#RowsetSchema".</span><span class="sxs-lookup"><span data-stu-id="88bda-118">The ID for the schema tag must be "RowsetSchema," and the namespace used to refer to the schema of the current rowset must point to "#RowsetSchema."</span></span>

<span data-ttu-id="88bda-119">Обратите внимание, что префикс пространства имен, который находится справа от толстой кишки и слева от равного знака, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="88bda-119">Note that the prefix of the namespace, that part to the right of the colon and to the left of the equal sign, is arbitrary.</span></span>

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

<span data-ttu-id="88bda-120">Пользователь может определить, что это любое имя, если это имя последовательно используется во всем XML-документе.</span><span class="sxs-lookup"><span data-stu-id="88bda-120">The user can define this to be any name as long as this name is consistently used throughout the XML document.</span></span> <span data-ttu-id="88bda-121">ADO всегда пишет "s", "rs", "dt" и "z", но эти имена префиксов не являются жестко закодироваться в компонент загрузки.</span><span class="sxs-lookup"><span data-stu-id="88bda-121">ADO always writes out "s," "rs," "dt," and "z," but these prefix names are not hard-coded into the loading component.</span></span>



