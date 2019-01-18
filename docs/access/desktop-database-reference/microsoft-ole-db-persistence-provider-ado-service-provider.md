---
title: Поставщик услуг хранения Microsoft OLE DB (поставщик служб ADO)
TOCTitle: Microsoft OLE DB Persistence Provider (ADO Service Provider)
ms:assetid: 22e41769-36eb-5a88-05ed-870938657624
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249007(v=office.15)
ms:contentKeyID: 48543719
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4045445120d42f1ca88fce22ce566fc970fce28b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715510"
---
# <a name="microsoft-ole-db-persistence-provider-ado-service-provider"></a><span data-ttu-id="ee653-102">Поставщик услуг хранения Microsoft OLE DB (поставщик служб ADO)</span><span class="sxs-lookup"><span data-stu-id="ee653-102">Microsoft OLE DB Persistence Provider (ADO Service Provider)</span></span>


<span data-ttu-id="ee653-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee653-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="ee653-104">Поставщик OLE DB сохраняемость позволяет сохранить объект [набора записей](recordset-object-ado.md) в файл и восстанавливать этот объект **набора записей** из файла.</span><span class="sxs-lookup"><span data-stu-id="ee653-104">The Microsoft OLE DB Persistence Provider enables you to save a [Recordset](recordset-object-ado.md) object into a file, and later restore that **Recordset** object from the file.</span></span> <span data-ttu-id="ee653-105">Сведения о схеме, данные и ожидающие изменения сохраняются.</span><span class="sxs-lookup"><span data-stu-id="ee653-105">Schema information, data, and pending changes are preserved.</span></span>

<span data-ttu-id="ee653-106">**Набор записей** можно сохранить в собственный формат дополнительные данные в таблице грамматики (ADTG) или форматов open языке (XML).</span><span class="sxs-lookup"><span data-stu-id="ee653-106">You can save the **Recordset** in either the proprietary Advanced Data Table Gram (ADTG) format, or the open Extensible Markup Language (XML) format.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="ee653-107">Ключевое слово поставщика</span><span class="sxs-lookup"><span data-stu-id="ee653-107">Provider Keyword</span></span>

<span data-ttu-id="ee653-108">Для вызова этого поставщика, укажите следующие ключевое слово и значение в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="ee653-108">To invoke this provider, specify the following keyword and value in the connection string.</span></span>

```vb 
 
"Provider=MSPersist" 
```

## <a name="errors"></a><span data-ttu-id="ee653-109">Ошибки</span><span class="sxs-lookup"><span data-stu-id="ee653-109">Errors</span></span>

<span data-ttu-id="ee653-110">В приложении могут быть обнаружены следующие ошибки, выданный данного поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee653-110">The following errors issued by this provider can be detected in your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee653-111">Константа</span><span class="sxs-lookup"><span data-stu-id="ee653-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="ee653-112">Описание</span><span class="sxs-lookup"><span data-stu-id="ee653-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee653-113">E_BADSTREAM</span><span class="sxs-lookup"><span data-stu-id="ee653-113">E_BADSTREAM</span></span></p></td>
<td><p><span data-ttu-id="ee653-114">Файл, открытый не имеет допустимый формат (то есть, формат не ADTG или XML).</span><span class="sxs-lookup"><span data-stu-id="ee653-114">The file opened does not have a valid format (that is, the format is not ADTG or XML).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee653-115">E_CANTPERSISTROWSET</span><span class="sxs-lookup"><span data-stu-id="ee653-115">E_CANTPERSISTROWSET</span></span></p></td>
<td><p><span data-ttu-id="ee653-116">Сохранить объект <strong>набора записей</strong> имеет характеристики, которые запретить сохранение.</span><span class="sxs-lookup"><span data-stu-id="ee653-116">The <strong>Recordset</strong> object saved has characteristics that prevent it from being stored.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ee653-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="ee653-117">Remarks</span></span>

<span data-ttu-id="ee653-118">Поставщик OLE DB сохраняемость предоставляет не динамические свойства.</span><span class="sxs-lookup"><span data-stu-id="ee653-118">The Microsoft OLE DB Persistence Provider exposes no dynamic properties.</span></span>

<span data-ttu-id="ee653-119">В настоящее время невозможно сохранить только параметризованный иерархических объекты **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="ee653-119">Currently, only parameterized hierarchical **Recordset** objects cannot be saved.</span></span>

<span data-ttu-id="ee653-120">Дополнительные сведения о постоянно хранение **записей** объектов [Набора записей](more-about-recordset-persistence.md)см.</span><span class="sxs-lookup"><span data-stu-id="ee653-120">For more information about persistently storing **Recordset** objects, see [Recordset Persistence](more-about-recordset-persistence.md).</span></span>

<span data-ttu-id="ee653-121">При использовании потока для открытия **набора записей**должен быть указаны никакие параметры, отличные от *источника* параметра метода **Open** .</span><span class="sxs-lookup"><span data-stu-id="ee653-121">When a stream is used to open a **Recordset**, there should be no parameters specified other than the *Source* parameter of the **Open** method.</span></span>

