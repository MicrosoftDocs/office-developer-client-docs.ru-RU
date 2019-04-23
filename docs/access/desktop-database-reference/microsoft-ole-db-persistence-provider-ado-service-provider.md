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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288955"
---
# <a name="microsoft-ole-db-persistence-provider-ado-service-provider"></a><span data-ttu-id="d8470-102">Поставщик услуг хранения Microsoft OLE DB (поставщик служб ADO)</span><span class="sxs-lookup"><span data-stu-id="d8470-102">Microsoft OLE DB Persistence Provider (ADO Service Provider)</span></span>


<span data-ttu-id="d8470-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d8470-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="d8470-104">Поставщик сохраняемости Microsoft OLE DB позволяет сохранить объект [Recordset](recordset-object-ado.md) в файле, а затем восстановить этот объект **Recordset** из файла.</span><span class="sxs-lookup"><span data-stu-id="d8470-104">The Microsoft OLE DB Persistence Provider enables you to save a [Recordset](recordset-object-ado.md) object into a file, and later restore that **Recordset** object from the file.</span></span> <span data-ttu-id="d8470-105">Сведения о схеме, данные и ожидающие изменения сохраняются.</span><span class="sxs-lookup"><span data-stu-id="d8470-105">Schema information, data, and pending changes are preserved.</span></span>

<span data-ttu-id="d8470-106">Вы можете сохранить **набор записей** в формате "особая таблица грамматики" (адтг) или формате Open Extensible Markup Language (XML).</span><span class="sxs-lookup"><span data-stu-id="d8470-106">You can save the **Recordset** in either the proprietary Advanced Data Table Gram (ADTG) format, or the open Extensible Markup Language (XML) format.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="d8470-107">Ключевое слово Provider</span><span class="sxs-lookup"><span data-stu-id="d8470-107">Provider Keyword</span></span>

<span data-ttu-id="d8470-108">Чтобы вызвать этот поставщик, укажите следующее ключевое слово и значение в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="d8470-108">To invoke this provider, specify the following keyword and value in the connection string.</span></span>

```vb 
 
"Provider=MSPersist" 
```

## <a name="errors"></a><span data-ttu-id="d8470-109">Ошибки</span><span class="sxs-lookup"><span data-stu-id="d8470-109">Errors</span></span>

<span data-ttu-id="d8470-110">Следующие ошибки, выданные поставщиком, могут быть обнаружены в приложении.</span><span class="sxs-lookup"><span data-stu-id="d8470-110">The following errors issued by this provider can be detected in your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8470-111">Константа</span><span class="sxs-lookup"><span data-stu-id="d8470-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="d8470-112">Описание</span><span class="sxs-lookup"><span data-stu-id="d8470-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8470-113">Е_БАДСТРЕАМ</span><span class="sxs-lookup"><span data-stu-id="d8470-113">E_BADSTREAM</span></span></p></td>
<td><p><span data-ttu-id="d8470-114">Открытый файл имеет недопустимый формат (то есть формат не АДТГ или XML).</span><span class="sxs-lookup"><span data-stu-id="d8470-114">The file opened does not have a valid format (that is, the format is not ADTG or XML).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8470-115">Е_КАНТПЕРСИСТРОВСЕТ</span><span class="sxs-lookup"><span data-stu-id="d8470-115">E_CANTPERSISTROWSET</span></span></p></td>
<td><p><span data-ttu-id="d8470-116">Сохраненный объект <strong>Recordset</strong> имеет характеристики, которые не позволяют сохранить его.</span><span class="sxs-lookup"><span data-stu-id="d8470-116">The <strong>Recordset</strong> object saved has characteristics that prevent it from being stored.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d8470-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="d8470-117">Remarks</span></span>

<span data-ttu-id="d8470-118">Поставщик сохраняемости Microsoft OLE DB не предоставляет динамические свойства.</span><span class="sxs-lookup"><span data-stu-id="d8470-118">The Microsoft OLE DB Persistence Provider exposes no dynamic properties.</span></span>

<span data-ttu-id="d8470-119">В настоящее время невозможно сохранить только параметризованные иерархические объекты **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="d8470-119">Currently, only parameterized hierarchical **Recordset** objects cannot be saved.</span></span>

<span data-ttu-id="d8470-120">Дополнительные сведения о постоянном хранении объектов **Recordset** можно найти в разделе Сохранение данных в [наборе записей](more-about-recordset-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="d8470-120">For more information about persistently storing **Recordset** objects, see [Recordset Persistence](more-about-recordset-persistence.md).</span></span>

<span data-ttu-id="d8470-121">Если для открытия объекта **Recordset**используется поток, параметры не должны быть указаны в параметре *Source* метода **Open** .</span><span class="sxs-lookup"><span data-stu-id="d8470-121">When a stream is used to open a **Recordset**, there should be no parameters specified other than the *Source* parameter of the **Open** method.</span></span>

