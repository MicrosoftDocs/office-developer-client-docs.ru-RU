---
title: Служба формирования данных (Майкрософт) для OLE DB (поставщик служб ADO)
TOCTitle: Microsoft Data Shaping Service for OLE DB (ADO Service Provider)
ms:assetid: 6e6e5f39-6f43-7c7b-5812-796096d1d31b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249436(v=office.15)
ms:contentKeyID: 48545511
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5065b966608f8d6a3ef1cb05be890b9a1f147dc8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288962"
---
# <a name="microsoft-data-shaping-service-for-ole-db-ado-service-provider"></a><span data-ttu-id="6a570-102">Служба формирования данных (Майкрософт) для OLE DB (поставщик служб ADO)</span><span class="sxs-lookup"><span data-stu-id="6a570-102">Microsoft Data Shaping Service for OLE DB (ADO Service Provider)</span></span>


<span data-ttu-id="6a570-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a570-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6a570-104">Служба формирования данных Майкрософт для поставщика услуг OLE DB поддерживает строительство иерархических (сформированных) объектов [Recordset](recordset-object-ado.md) от поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="6a570-104">The Microsoft Data Shaping Service for OLE DB service provider supports the construction of hierarchical (shaped) [Recordset](recordset-object-ado.md) objects from a data provider.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="6a570-105">Ключевое слово поставщика</span><span class="sxs-lookup"><span data-stu-id="6a570-105">Provider Keyword</span></span>

<span data-ttu-id="6a570-106">Чтобы вызвать службу формирования данных для OLE DB, укажите следующее ключевое слово и значение в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="6a570-106">To invoke the Data Shaping Service for OLE DB, specify the following keyword and value in the connection string.</span></span>

```vb 
 
"Provider=MSDataShape" 
```

## <a name="dynamic-properties"></a><span data-ttu-id="6a570-107">Dynamic Properties</span><span class="sxs-lookup"><span data-stu-id="6a570-107">Dynamic Properties</span></span>

<span data-ttu-id="6a570-108">При вызове этого поставщика услуг в коллекцию Свойств объекта [Подключения](connection-object-ado.md) добавляются следующие [динамические](properties-collection-ado.md) свойства.</span><span class="sxs-lookup"><span data-stu-id="6a570-108">When this service provider is invoked, the following dynamic properties are added to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6a570-109">Динамическое имя свойства</span><span class="sxs-lookup"><span data-stu-id="6a570-109">Dynamic Property Name</span></span></p></th>
<th><p><span data-ttu-id="6a570-110">Description</span><span class="sxs-lookup"><span data-stu-id="6a570-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a570-111"><strong>Уникальные имена для переописи</strong></span><span class="sxs-lookup"><span data-stu-id="6a570-111"><strong>Unique Reshape Names</strong></span></span></p></td>
<td><p><span data-ttu-id="6a570-112">Указывает, разрешены ли <strong>объекты Recordset</strong> с дублирующими значениями для свойств <strong>reshape Name.</strong></span><span class="sxs-lookup"><span data-stu-id="6a570-112">Indicates whether <strong>Recordset</strong> objects with duplicate values for their <strong>Reshape Name</strong> properties are allowed.</span></span> <span data-ttu-id="6a570-113">Если это динамическое свойство <strong>True</strong> и создается новый <strong>набор</strong> записей с таким же имям изменения, что и существующее имя <strong>Recordset,</strong>то новое имя объекта <strong>Recordset</strong> изменено, чтобы сделать его уникальным.</span><span class="sxs-lookup"><span data-stu-id="6a570-113">If this dynamic property is <strong>True</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as an existing <strong>Recordset</strong>, then the new <strong>Recordset</strong> object's reshape name is modified to make it unique.</span></span> <span data-ttu-id="6a570-114">Если это <strong></strong> свойство false и создается новый <strong>набор записей</strong> с тем же имям переостановки, что и существующий <strong>recordset,</strong>то оба объекта <strong>Recordset</strong> будут иметь такое же имя.</span><span class="sxs-lookup"><span data-stu-id="6a570-114">If this property is <strong>False</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as the existing <strong>Recordset</strong>, both <strong>Recordset</strong> objects will have the same reshape name.</span></span> <span data-ttu-id="6a570-115">Поэтому ни <strong>один из наборов записей</strong> не может быть переделен до тех пор, пока существуют оба эти набора.</span><span class="sxs-lookup"><span data-stu-id="6a570-115">Therefore, neither <strong>Recordset</strong> can be reshaped as long as both recordsets exist.</span></span> <span data-ttu-id="6a570-116">По умолчанию значение свойства <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="6a570-116">The default value of the property is <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a570-117"><strong>Поставщик данных</strong></span><span class="sxs-lookup"><span data-stu-id="6a570-117"><strong>Data Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="6a570-118">Указывает имя поставщика, который будет поставлять строки для фигуры.</span><span class="sxs-lookup"><span data-stu-id="6a570-118">Indicates the name of the provider that will supply rows to be shaped.</span></span> <span data-ttu-id="6a570-119">Это значение может быть NONE, если поставщик не будет использоваться для поставки строк.</span><span class="sxs-lookup"><span data-stu-id="6a570-119">This value may be NONE if a provider will not be used to supply rows.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6a570-120">Можно также задать подавные динамические свойства, указав их имена в качестве ключевых слов в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="6a570-120">You may also set writable dynamic properties by specifying their names as keywords in the connection string.</span></span> <span data-ttu-id="6a570-121">Например, в microsoft Visual Basic установите динамическое свойство **поставщика** данных на "MSDASQL", указав:</span><span class="sxs-lookup"><span data-stu-id="6a570-121">For example, in Microsoft Visual Basic, set the **Data Provider** dynamic property to "MSDASQL" by specifying:</span></span>

```vb 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MSDataShape;Data Provider=MSDASQL" 
```

<span data-ttu-id="6a570-122">Вы также можете задать или получить динамическое свойство, указав его имя в качестве индекса свойства [свойства.](properties-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="6a570-122">You may also set or retrieve a dynamic property by specifying its name as the index to the [Properties](properties-collection-ado.md) property.</span></span> <span data-ttu-id="6a570-123">Например, получите и распечатайте текущее значение динамического свойства **поставщика** данных, а затем установите новое значение, например:</span><span class="sxs-lookup"><span data-stu-id="6a570-123">For example, get and print the current value of the **Data Provider** dynamic property, then set a new value, like this:</span></span>

```vb 
 
Debug.Print cn.Properties("Data Provider") 
cn.Properties("Data Provider") = "MSDASQL" 
```

<span data-ttu-id="6a570-124">Дополнительные сведения о формировании данных см. в [дополнительных сведениях о формировании данных.](data-shaping.md)</span><span class="sxs-lookup"><span data-stu-id="6a570-124">For more information about data shaping, see [Data Shaping](data-shaping.md).</span></span>

