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
# <a name="microsoft-data-shaping-service-for-ole-db-ado-service-provider"></a><span data-ttu-id="c2e96-102">Служба формирования данных (Майкрософт) для OLE DB (поставщик служб ADO)</span><span class="sxs-lookup"><span data-stu-id="c2e96-102">Microsoft Data Shaping Service for OLE DB (ADO Service Provider)</span></span>


<span data-ttu-id="c2e96-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2e96-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c2e96-104">Служба формирования данных Майкрософт для поставщика службы OLE DB поддерживает конструкцию объектов [recordset](recordset-object-ado.md) иерархических (в виде) из поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="c2e96-104">The Microsoft Data Shaping Service for OLE DB service provider supports the construction of hierarchical (shaped) [Recordset](recordset-object-ado.md) objects from a data provider.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="c2e96-105">Ключевое слово поставщика</span><span class="sxs-lookup"><span data-stu-id="c2e96-105">Provider Keyword</span></span>

<span data-ttu-id="c2e96-106">Чтобы вызвать службу формирования данных для OLE DB, укажите следующее ключевое слово и значение в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="c2e96-106">To invoke the Data Shaping Service for OLE DB, specify the following keyword and value in the connection string.</span></span>

```vb 
 
"Provider=MSDataShape" 
```

## <a name="dynamic-properties"></a><span data-ttu-id="c2e96-107">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="c2e96-107">Dynamic Properties</span></span>

<span data-ttu-id="c2e96-108">При вызове этого поставщика службы в коллекцию свойств объекта [Connection](connection-object-ado.md) добавляются следующие [динамические](properties-collection-ado.md) свойства.</span><span class="sxs-lookup"><span data-stu-id="c2e96-108">When this service provider is invoked, the following dynamic properties are added to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c2e96-109">Динамическое имя свойства</span><span class="sxs-lookup"><span data-stu-id="c2e96-109">Dynamic Property Name</span></span></p></th>
<th><p><span data-ttu-id="c2e96-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c2e96-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c2e96-111"><strong>Уникальные имена для повторнойshape</strong></span><span class="sxs-lookup"><span data-stu-id="c2e96-111"><strong>Unique Reshape Names</strong></span></span></p></td>
<td><p><span data-ttu-id="c2e96-112">Указывает, разрешены <strong>ли объекты Recordset</strong> с дублирующимися значениями для их свойств <strong>reshape Name.</strong></span><span class="sxs-lookup"><span data-stu-id="c2e96-112">Indicates whether <strong>Recordset</strong> objects with duplicate values for their <strong>Reshape Name</strong> properties are allowed.</span></span> <span data-ttu-id="c2e96-113">Если это динамическое свойство имеет true и создается новый набор <strong>записей</strong> с таким же именем повторнойshape, заданным пользователем, как у существующего объекта <strong></strong> <strong>Recordset,</strong>то имя нового объекта <strong>Recordset</strong> в reshape будет изменено, чтобы сделать его уникальным.</span><span class="sxs-lookup"><span data-stu-id="c2e96-113">If this dynamic property is <strong>True</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as an existing <strong>Recordset</strong>, then the new <strong>Recordset</strong> object's reshape name is modified to make it unique.</span></span> <span data-ttu-id="c2e96-114">Если это свойство имеет свойство <strong>False</strong> и создается новый объект <strong>Recordset</strong> с таким же именем повторнойshape, заданным пользователем, как у существующего объекта <strong>Recordset,</strong>то оба объекта <strong>Recordset</strong> будут иметь такое же имя повторнойshape.</span><span class="sxs-lookup"><span data-stu-id="c2e96-114">If this property is <strong>False</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as the existing <strong>Recordset</strong>, both <strong>Recordset</strong> objects will have the same reshape name.</span></span> <span data-ttu-id="c2e96-115">Таким образом, ни <strong>один из наборов записей</strong> не может быть повторно скомелен, пока существуют оба наборы записей.</span><span class="sxs-lookup"><span data-stu-id="c2e96-115">Therefore, neither <strong>Recordset</strong> can be reshaped as long as both recordsets exist.</span></span> <span data-ttu-id="c2e96-116">Значение свойства по умолчанию — <strong>False.</strong></span><span class="sxs-lookup"><span data-stu-id="c2e96-116">The default value of the property is <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2e96-117"><strong>Поставщик данных</strong></span><span class="sxs-lookup"><span data-stu-id="c2e96-117"><strong>Data Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="c2e96-118">Указывает имя поставщика, который будет указывать строки для фигуры.</span><span class="sxs-lookup"><span data-stu-id="c2e96-118">Indicates the name of the provider that will supply rows to be shaped.</span></span> <span data-ttu-id="c2e96-119">Это значение может быть NONE, если поставщик не будет использоваться для предложения строк.</span><span class="sxs-lookup"><span data-stu-id="c2e96-119">This value may be NONE if a provider will not be used to supply rows.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c2e96-120">Можно также задать динамические свойства, которые можно переписать, указав их имена в качестве ключевых слов в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="c2e96-120">You may also set writable dynamic properties by specifying their names as keywords in the connection string.</span></span> <span data-ttu-id="c2e96-121">Например, в Microsoft Visual Basic для динамического свойства **поставщика** данных установите для динамического свойства "MSDASQL", указав:</span><span class="sxs-lookup"><span data-stu-id="c2e96-121">For example, in Microsoft Visual Basic, set the **Data Provider** dynamic property to "MSDASQL" by specifying:</span></span>

```vb 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MSDataShape;Data Provider=MSDASQL" 
```

<span data-ttu-id="c2e96-122">Вы также можете задать или получить динамическое свойство, указав его имя в качестве индекса [для свойства Properties.](properties-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="c2e96-122">You may also set or retrieve a dynamic property by specifying its name as the index to the [Properties](properties-collection-ado.md) property.</span></span> <span data-ttu-id="c2e96-123">Например, получите и распечатайте текущее значение динамического свойства **поставщика** данных, а затем установите новое значение, например:</span><span class="sxs-lookup"><span data-stu-id="c2e96-123">For example, get and print the current value of the **Data Provider** dynamic property, then set a new value, like this:</span></span>

```vb 
 
Debug.Print cn.Properties("Data Provider") 
cn.Properties("Data Provider") = "MSDASQL" 
```

<span data-ttu-id="c2e96-124">Дополнительные сведения о формировании данных [см. в теме "Формирование данных".](data-shaping.md)</span><span class="sxs-lookup"><span data-stu-id="c2e96-124">For more information about data shaping, see [Data Shaping](data-shaping.md).</span></span>

