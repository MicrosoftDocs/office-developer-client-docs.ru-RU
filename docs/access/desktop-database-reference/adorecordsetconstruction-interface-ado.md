---
title: Интерфейс ADORecordsetConstruction (ADO)
TOCTitle: ADORecordsetConstruction Interface (ADO)
ms:assetid: 2b53aa6e-3b6f-a996-3967-534215fd586c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249060(v=office.15)
ms:contentKeyID: 48543926
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c7ea33eb0cdd221f0d59edfb7cd04520bb888249
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877403"
---
# <a name="adorecordsetconstruction-interface-ado"></a><span data-ttu-id="13f3d-102">Интерфейс ADORecordsetConstruction (ADO)</span><span class="sxs-lookup"><span data-stu-id="13f3d-102">ADORecordsetConstruction Interface (ADO)</span></span>


<span data-ttu-id="13f3d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="13f3d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="13f3d-104">Интерфейс **ADORecordsetConstruction** используется для создания объекта ADO **записей** из объекта OLE DB **строк** в приложении C/C++.</span><span class="sxs-lookup"><span data-stu-id="13f3d-104">The **ADORecordsetConstruction** interface is used to construct an ADO **Recordset** object from an OLE DB **Rowset** object in a C/C++ application.</span></span>

<span data-ttu-id="13f3d-105">Этот интерфейс поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="13f3d-105">This interface supports the following properties:</span></span>

## <a name="properties"></a><span data-ttu-id="13f3d-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="13f3d-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13f3d-107"><a href="chapter-property-ado.md">Главы</a></span><span class="sxs-lookup"><span data-stu-id="13f3d-107"><a href="chapter-property-ado.md">Chapter</a></span></span></p></td>
<td><p><span data-ttu-id="13f3d-108">Чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="13f3d-108">Read/Write.</span></span><br />
<span data-ttu-id="13f3d-109">Получает или задает объект OLE DB <strong>главы</strong> из/на этот объект ADO <strong>Recordset</strong> .</span><span class="sxs-lookup"><span data-stu-id="13f3d-109">Gets/sets an OLE DB <strong>Chapter</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13f3d-110"><a href="rowposition-property-ado.md">RowPosition</a></span><span class="sxs-lookup"><span data-stu-id="13f3d-110"><a href="rowposition-property-ado.md">RowPosition</a></span></span></p></td>
<td><p><span data-ttu-id="13f3d-111">Чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="13f3d-111">Read/Write.</span></span><br />
<span data-ttu-id="13f3d-112">Получает или задает объект OLE DB <strong>RowPosition</strong> из/на этот объект ADO <strong>Recordset</strong> .</span><span class="sxs-lookup"><span data-stu-id="13f3d-112">Gets/sets an OLE DB <strong>RowPosition</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13f3d-113"><a href="rowset-property-ado.md">Набор строк</a></span><span class="sxs-lookup"><span data-stu-id="13f3d-113"><a href="rowset-property-ado.md">Rowset</a></span></span></p></td>
<td><p><span data-ttu-id="13f3d-114">Чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="13f3d-114">Read/Write.</span></span><br />
<span data-ttu-id="13f3d-115">Получает или задает объект OLE DB <strong>строк</strong> из/на этот объект ADO <strong>Recordset</strong> .</span><span class="sxs-lookup"><span data-stu-id="13f3d-115">Gets/sets an OLE DB <strong>Rowset</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a><span data-ttu-id="13f3d-116">Методы</span><span class="sxs-lookup"><span data-stu-id="13f3d-116">Methods</span></span>

<span data-ttu-id="13f3d-117">Отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="13f3d-117">None.</span></span>

## <a name="events"></a><span data-ttu-id="13f3d-118">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="13f3d-118">Events</span></span>

<span data-ttu-id="13f3d-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="13f3d-119">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="13f3d-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="13f3d-120">Remarks</span></span>

<span data-ttu-id="13f3d-121">Получает объект OLE DB **строк** (pRowset), конструкции (объект ADO **набора записей** ), конструкции суммы (adoRs) объект ADO **набора записей** к три базовых операций:</span><span class="sxs-lookup"><span data-stu-id="13f3d-121">Given an OLE DB **Rowset** object (pRowset ), the construction of an ADO **Recordset** object (), the construction of an ADO **Recordset** object (adoRs ) amounts to the following three basic operations:</span></span>

1. <span data-ttu-id="13f3d-122">Создайте объект ADO **набора записей** :</span><span class="sxs-lookup"><span data-stu-id="13f3d-122">Create an ADO **Recordset** object:</span></span>
    
   ```vb
    Recordset20Ptr adoRs;
    adoRs.CreateInstance(__uuidof(Recordset));
   ```
2. <span data-ttu-id="13f3d-123">Запрос интерфейс **IADORecordsetConstruction** объекта **набора записей** :</span><span class="sxs-lookup"><span data-stu-id="13f3d-123">Query the **IADORecordsetConstruction** interface on the **Recordset** object:</span></span>

   ```vb    
    adoRecordsetConstructionPtr adoRsConstruct=NULL;
    adoRs->QueryInterface(__uuidof(ADORecordsetConstruction),
         (void**)&adoRsConstruct);
   ```

3. <span data-ttu-id="13f3d-124">Вызов IADORecordsetConstruction::put\_метод свойства строк установить объект строк OLE DB для объекта набора записей ADO:</span><span class="sxs-lookup"><span data-stu-id="13f3d-124">Call the IADORecordsetConstruction::put\_Rowset property method to set the OLE DB Rowset object on the ADO Recordset object:</span></span>

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
<span data-ttu-id="13f3d-125">Результирующий объект теперь представляет объект ADO **записей** , созданный из объекта OLE DB **строк** .</span><span class="sxs-lookup"><span data-stu-id="13f3d-125">The resultant object now represents the ADO **Recordset** object constructed from the OLE DB **Rowset** object.</span></span>

<span data-ttu-id="13f3d-126">Также можно создать объект ADO **записей** из объекта OLE DB **главы** или **RowPosition** .</span><span class="sxs-lookup"><span data-stu-id="13f3d-126">You can also construct an ADO **Recordset** object from an OLE DB **Chapter** or **RowPosition** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="13f3d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="13f3d-127">Requirements</span></span>

- <span data-ttu-id="13f3d-128">**Версия:** ADO 2.0 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="13f3d-128">**Version:** ADO 2.0 and later</span></span>

- <span data-ttu-id="13f3d-129">**Библиотеки:** msado15.dll</span><span class="sxs-lookup"><span data-stu-id="13f3d-129">**Library:** msado15.dll</span></span>

- <span data-ttu-id="13f3d-130">**UUID:** 00000283-0000-0010-8000-00AA006D2EA4</span><span class="sxs-lookup"><span data-stu-id="13f3d-130">**UUID:** 00000283-0000-0010-8000-00AA006D2EA4</span></span>

