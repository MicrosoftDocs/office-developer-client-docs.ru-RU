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
# <a name="microsoft-ole-db-persistence-provider-ado-service-provider"></a><span data-ttu-id="34fe0-102">Поставщик услуг хранения Microsoft OLE DB (поставщик служб ADO)</span><span class="sxs-lookup"><span data-stu-id="34fe0-102">Microsoft OLE DB Persistence Provider (ADO Service Provider)</span></span>


<span data-ttu-id="34fe0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="34fe0-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="34fe0-104">Поставщик сохраняемости Microsoft OLE DB позволяет сохранить объект [Recordset](recordset-object-ado.md) в файле, а затем восстановить объект **Recordset** из файла.</span><span class="sxs-lookup"><span data-stu-id="34fe0-104">The Microsoft OLE DB Persistence Provider enables you to save a [Recordset](recordset-object-ado.md) object into a file, and later restore that **Recordset** object from the file.</span></span> <span data-ttu-id="34fe0-105">Сведения о схеме, данные и ожидающих изменений сохраняются.</span><span class="sxs-lookup"><span data-stu-id="34fe0-105">Schema information, data, and pending changes are preserved.</span></span>

<span data-ttu-id="34fe0-106">Можно сохранить набор **записей** либо в фирменом формате Advanced Data Table Gram (ADTG), либо в формате open Extensible Markup Language (XML).</span><span class="sxs-lookup"><span data-stu-id="34fe0-106">You can save the **Recordset** in either the proprietary Advanced Data Table Gram (ADTG) format, or the open Extensible Markup Language (XML) format.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="34fe0-107">Ключевое слово поставщика</span><span class="sxs-lookup"><span data-stu-id="34fe0-107">Provider Keyword</span></span>

<span data-ttu-id="34fe0-108">Чтобы вызвать этого поставщика, укажите следующее ключевое слово и значение в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="34fe0-108">To invoke this provider, specify the following keyword and value in the connection string.</span></span>

```vb 
 
"Provider=MSPersist" 
```

## <a name="errors"></a><span data-ttu-id="34fe0-109">Ошибки</span><span class="sxs-lookup"><span data-stu-id="34fe0-109">Errors</span></span>

<span data-ttu-id="34fe0-110">Следующие ошибки, выданные этим поставщиком, можно обнаружить в вашем приложении.</span><span class="sxs-lookup"><span data-stu-id="34fe0-110">The following errors issued by this provider can be detected in your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="34fe0-111">Константа</span><span class="sxs-lookup"><span data-stu-id="34fe0-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="34fe0-112">Описание</span><span class="sxs-lookup"><span data-stu-id="34fe0-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34fe0-113">E_BADSTREAM</span><span class="sxs-lookup"><span data-stu-id="34fe0-113">E_BADSTREAM</span></span></p></td>
<td><p><span data-ttu-id="34fe0-114">Открытый файл не имеет допустимый формат (то есть формат не ADTG или XML).</span><span class="sxs-lookup"><span data-stu-id="34fe0-114">The file opened does not have a valid format (that is, the format is not ADTG or XML).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34fe0-115">E_CANTPERSISTROWSET</span><span class="sxs-lookup"><span data-stu-id="34fe0-115">E_CANTPERSISTROWSET</span></span></p></td>
<td><p><span data-ttu-id="34fe0-116">Сохраненный <strong>объект Recordset</strong> имеет характеристики, которые мешают ему храниться.</span><span class="sxs-lookup"><span data-stu-id="34fe0-116">The <strong>Recordset</strong> object saved has characteristics that prevent it from being stored.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="34fe0-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="34fe0-117">Remarks</span></span>

<span data-ttu-id="34fe0-118">Поставщик сохраняемости Microsoft OLE DB не предоставляет динамические свойства.</span><span class="sxs-lookup"><span data-stu-id="34fe0-118">The Microsoft OLE DB Persistence Provider exposes no dynamic properties.</span></span>

<span data-ttu-id="34fe0-119">В настоящее время невозможно сохранить только параметризированные объекты **иерархического набора** записей.</span><span class="sxs-lookup"><span data-stu-id="34fe0-119">Currently, only parameterized hierarchical **Recordset** objects cannot be saved.</span></span>

<span data-ttu-id="34fe0-120">Дополнительные сведения о постоянном хранении объектов **Recordset** см. в дополнительных [сведениях о сохраняемом сохраняемом наборе данных.](more-about-recordset-persistence.md)</span><span class="sxs-lookup"><span data-stu-id="34fe0-120">For more information about persistently storing **Recordset** objects, see [Recordset Persistence](more-about-recordset-persistence.md).</span></span>

<span data-ttu-id="34fe0-121">Когда поток используется для открытия **наборов записей,** не должно быть параметров, заданных, кроме *параметра Source* метода **Open.**</span><span class="sxs-lookup"><span data-stu-id="34fe0-121">When a stream is used to open a **Recordset**, there should be no parameters specified other than the *Source* parameter of the **Open** method.</span></span>

