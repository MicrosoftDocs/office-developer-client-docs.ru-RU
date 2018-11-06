---
title: Пространства имен (Справочник по для настольных баз данных Access)
TOCTitle: Namespaces
ms:assetid: e39f003c-3d16-1fae-48c5-304593c41f2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250158(v=office.15)
ms:contentKeyID: 48548318
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a5fb61c02a5679c6fd63e9d5dd2a257ab5f7d96a
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996470"
---
# <a name="namespaces"></a><span data-ttu-id="51db7-102">Пространства имен</span><span class="sxs-lookup"><span data-stu-id="51db7-102">Namespaces</span></span>

<span data-ttu-id="51db7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51db7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51db7-104">Формат сохранения XML в ADO использует следующие четыре пространства имен.</span><span class="sxs-lookup"><span data-stu-id="51db7-104">The XML persistence format in ADO uses the following four namespaces.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51db7-105">Префикс</span><span class="sxs-lookup"><span data-stu-id="51db7-105">Prefix</span></span></p></th>
<th><p><span data-ttu-id="51db7-106">Описание</span><span class="sxs-lookup"><span data-stu-id="51db7-106">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51db7-107">s</span><span class="sxs-lookup"><span data-stu-id="51db7-107">s</span></span></p></td>
<td><p><span data-ttu-id="51db7-108">Относится к &quot;XML-данные&quot; пространства имен, содержащего элементы и атрибуты, которые определяют схемы текущего <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="51db7-108">Refers to the &quot;XML-Data&quot; namespace containing the elements and attributes that define the schema of the current <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51db7-109">dt</span><span class="sxs-lookup"><span data-stu-id="51db7-109">dt</span></span></p></td>
<td><p><span data-ttu-id="51db7-110">Относится к спецификации определения типа данных.</span><span class="sxs-lookup"><span data-stu-id="51db7-110">Refers to the data type definitions specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51db7-111">RS</span><span class="sxs-lookup"><span data-stu-id="51db7-111">rs</span></span></p></td>
<td><p><span data-ttu-id="51db7-112">Относится к области имен, содержащие элементы и атрибуты, относящиеся к свойствам ADO <strong>записей</strong> и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="51db7-112">Refers to the namespace containing elements and attributes specific to ADO <strong>Recordset</strong> properties and attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51db7-113">z</span><span class="sxs-lookup"><span data-stu-id="51db7-113">z</span></span></p></td>
<td><p><span data-ttu-id="51db7-114">Относится к схеме текущий набор строк.</span><span class="sxs-lookup"><span data-stu-id="51db7-114">Refers to the schema of the current rowset.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="51db7-115">Клиент не следует добавлять собственные теги следующие пространства имен, определенный в спецификации.</span><span class="sxs-lookup"><span data-stu-id="51db7-115">A client should not add its own tags to these namespaces, as defined by the specification.</span></span> <span data-ttu-id="51db7-116">Например, клиент не задавайте имен как «urn: schemas-microsoft-com:rowset» и затем записать что-нибудь, например «rs: MyOwnTag.»</span><span class="sxs-lookup"><span data-stu-id="51db7-116">For example, a client should not define a namespace as "urn:schemas-microsoft-com:rowset" and then write out something such as "rs:MyOwnTag."</span></span> <span data-ttu-id="51db7-117">Дополнительные сведения о пространствах имен [XML](https://www.w3.org/tr/xml-names/)см.</span><span class="sxs-lookup"><span data-stu-id="51db7-117">To learn more about namespaces, see [XML Namespaces](https://www.w3.org/tr/xml-names/).</span></span>

> [!NOTE]
> <span data-ttu-id="51db7-118">Идентификатор для тега схемы должен быть «RowsetSchema» и пространство имен, используемое для ссылки на схему текущий набор строк должен указывать «#RowsetSchema».</span><span class="sxs-lookup"><span data-stu-id="51db7-118">The ID for the schema tag must be "RowsetSchema," and the namespace used to refer to the schema of the current rowset must point to "#RowsetSchema."</span></span>

<span data-ttu-id="51db7-119">Обратите внимание, что префикс пространства имен, в правой части двоеточие и слева от знака равенства, произвольных.</span><span class="sxs-lookup"><span data-stu-id="51db7-119">Note that the prefix of the namespace, that part to the right of the colon and to the left of the equal sign, is arbitrary.</span></span>

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

<span data-ttu-id="51db7-120">Пользователь может указать это будет любое имя, поскольку это имя будет использоваться постоянно в XML-документ.</span><span class="sxs-lookup"><span data-stu-id="51db7-120">The user can define this to be any name as long as this name is consistently used throughout the XML document.</span></span> <span data-ttu-id="51db7-121">ADO всегда считывает «s,» «rs», «dt» и «z», но эти имена префикс не жестко в компонент загрузки.</span><span class="sxs-lookup"><span data-stu-id="51db7-121">ADO always writes out "s," "rs," "dt," and "z," but these prefix names are not hard-coded into the loading component.</span></span>



