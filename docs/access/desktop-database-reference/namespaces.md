---
title: Пространства имен (Справочник по базам данных Access на компьютере)
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
# <a name="namespaces"></a><span data-ttu-id="1be1e-102">Пространства имен</span><span class="sxs-lookup"><span data-stu-id="1be1e-102">Namespaces</span></span>

<span data-ttu-id="1be1e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1be1e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1be1e-104">Формат сохраняемости XML в ADO использует следующие четыре пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1be1e-104">The XML persistence format in ADO uses the following four namespaces.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1be1e-105">Prefix</span><span class="sxs-lookup"><span data-stu-id="1be1e-105">Prefix</span></span></p></th>
<th><p><span data-ttu-id="1be1e-106">Описание</span><span class="sxs-lookup"><span data-stu-id="1be1e-106">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1be1e-107">s</span><span class="sxs-lookup"><span data-stu-id="1be1e-107">s</span></span></p></td>
<td><p><span data-ttu-id="1be1e-108">Указывает пространство имен &quot;XML-данных&quot; , содержащее элементы и атрибуты, определяющие схему текущего <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="1be1e-108">Refers to the &quot;XML-Data&quot; namespace containing the elements and attributes that define the schema of the current <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be1e-109">Microsof</span><span class="sxs-lookup"><span data-stu-id="1be1e-109">dt</span></span></p></td>
<td><p><span data-ttu-id="1be1e-110">Ссылается на спецификацию определений типов данных.</span><span class="sxs-lookup"><span data-stu-id="1be1e-110">Refers to the data type definitions specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1be1e-111">кабел</span><span class="sxs-lookup"><span data-stu-id="1be1e-111">rs</span></span></p></td>
<td><p><span data-ttu-id="1be1e-112">Ссылается на пространство имен, содержащее элементы и атрибуты, относящиеся к свойствам и атрибутам <strong>Recordset</strong> объекта ADO.</span><span class="sxs-lookup"><span data-stu-id="1be1e-112">Refers to the namespace containing elements and attributes specific to ADO <strong>Recordset</strong> properties and attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1be1e-113">z</span><span class="sxs-lookup"><span data-stu-id="1be1e-113">z</span></span></p></td>
<td><p><span data-ttu-id="1be1e-114">Ссылается на схему текущего набора строк.</span><span class="sxs-lookup"><span data-stu-id="1be1e-114">Refers to the schema of the current rowset.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1be1e-115">Клиент не должен добавлять собственные теги к этим пространствам имен, как определено в спецификации.</span><span class="sxs-lookup"><span data-stu-id="1be1e-115">A client should not add its own tags to these namespaces, as defined by the specification.</span></span> <span data-ttu-id="1be1e-116">Например, клиент не должен определять пространство имен как "urn: schemas-microsoft-com: RowSet", а затем записывать что-то вроде "RS: Мйовнтаг".</span><span class="sxs-lookup"><span data-stu-id="1be1e-116">For example, a client should not define a namespace as "urn:schemas-microsoft-com:rowset" and then write out something such as "rs:MyOwnTag."</span></span> <span data-ttu-id="1be1e-117">Дополнительные сведения о пространствах имен содержатся в разделе [пространства имен XML](https://www.w3.org/tr/xml-names/).</span><span class="sxs-lookup"><span data-stu-id="1be1e-117">To learn more about namespaces, see [XML Namespaces](https://www.w3.org/tr/xml-names/).</span></span>

> [!NOTE]
> <span data-ttu-id="1be1e-118">ИДЕНТИФИКАТОР тега схемы должен иметь значение "Ровсетсчема", а пространство имен, используемое для ссылки на схему текущего набора строк, должно указывать на "#RowsetSchema".</span><span class="sxs-lookup"><span data-stu-id="1be1e-118">The ID for the schema tag must be "RowsetSchema," and the namespace used to refer to the schema of the current rowset must point to "#RowsetSchema."</span></span>

<span data-ttu-id="1be1e-119">Обратите внимание, что префикс пространства имен, который является частью справа от двоеточия и слева от знака равенства, является произвольным.</span><span class="sxs-lookup"><span data-stu-id="1be1e-119">Note that the prefix of the namespace, that part to the right of the colon and to the left of the equal sign, is arbitrary.</span></span>

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

<span data-ttu-id="1be1e-120">Пользователь может задать любое имя, если это имя постоянно используется в пределах XML-документа.</span><span class="sxs-lookup"><span data-stu-id="1be1e-120">The user can define this to be any name as long as this name is consistently used throughout the XML document.</span></span> <span data-ttu-id="1be1e-121">ADO всегда записывает "s", "RS", "DT" и "z", но эти имена префиксов не жестко задаются в компонент загрузки.</span><span class="sxs-lookup"><span data-stu-id="1be1e-121">ADO always writes out "s," "rs," "dt," and "z," but these prefix names are not hard-coded into the loading component.</span></span>



