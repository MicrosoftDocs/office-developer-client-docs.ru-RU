---
title: Интерфейс ADORecordsetConstruction (ADO)
TOCTitle: ADORecordsetConstruction interface (ADO)
ms:assetid: 2b53aa6e-3b6f-a996-3967-534215fd586c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249060(v=office.15)
ms:contentKeyID: 48543926
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 98342d5456c545e6da8539c11f616c08fd52a932
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281635"
---
# <a name="adorecordsetconstruction-interface-ado"></a><span data-ttu-id="8f672-102">Интерфейс ADORecordsetConstruction (ADO)</span><span class="sxs-lookup"><span data-stu-id="8f672-102">ADORecordsetConstruction interface (ADO)</span></span>


<span data-ttu-id="8f672-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8f672-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8f672-104">Интерфейс **ADORecordsetConstruction** используется для создания объекта ADO **Recordset** из объекта **набора строк** OLE DB в приложении C/C++.</span><span class="sxs-lookup"><span data-stu-id="8f672-104">The **ADORecordsetConstruction** interface is used to construct an ADO **Recordset** object from an OLE DB **Rowset** object in a C/C++ application.</span></span>

<span data-ttu-id="8f672-105">Этот интерфейс поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="8f672-105">This interface supports the following properties:</span></span>

## <a name="properties"></a><span data-ttu-id="8f672-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="8f672-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f672-107"><a href="chapter-property-ado.md">Части</a></span><span class="sxs-lookup"><span data-stu-id="8f672-107"><a href="chapter-property-ado.md">Chapter</a></span></span></p></td>
<td><p><span data-ttu-id="8f672-108">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="8f672-108">Read/Write.</span></span><br />
<span data-ttu-id="8f672-109">Получает или задает объект <strong>главы</strong> OLE DB от или on этого объекта <strong>Recordset</strong> ADO.</span><span class="sxs-lookup"><span data-stu-id="8f672-109">Gets/sets an OLE DB <strong>Chapter</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f672-110"><a href="rowposition-property-ado.md">RowPosition</a></span><span class="sxs-lookup"><span data-stu-id="8f672-110"><a href="rowposition-property-ado.md">RowPosition</a></span></span></p></td>
<td><p><span data-ttu-id="8f672-111">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="8f672-111">Read/Write.</span></span><br />
<span data-ttu-id="8f672-112">Получает/устанавливает объект <strong>ROWPOSITION</strong> OLE DB from/On этого объекта <strong>Recordset</strong> ADO.</span><span class="sxs-lookup"><span data-stu-id="8f672-112">Gets/sets an OLE DB <strong>RowPosition</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f672-113"><a href="rowset-property-ado.md">Возвращаем</a></span><span class="sxs-lookup"><span data-stu-id="8f672-113"><a href="rowset-property-ado.md">Rowset</a></span></span></p></td>
<td><p><span data-ttu-id="8f672-114">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="8f672-114">Read/Write.</span></span><br />
<span data-ttu-id="8f672-115">Получает или задает объект <strong>набора строк</strong> OLE DB from/On этого объекта <strong>Recordset</strong> ADO.</span><span class="sxs-lookup"><span data-stu-id="8f672-115">Gets/sets an OLE DB <strong>Rowset</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a><span data-ttu-id="8f672-116">Методы</span><span class="sxs-lookup"><span data-stu-id="8f672-116">Methods</span></span>

<span data-ttu-id="8f672-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="8f672-117">None.</span></span>

## <a name="events"></a><span data-ttu-id="8f672-118">События</span><span class="sxs-lookup"><span data-stu-id="8f672-118">Events</span></span>

<span data-ttu-id="8f672-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="8f672-119">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f672-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="8f672-120">Remarks</span></span>

<span data-ttu-id="8f672-121">При наличии объекта **набора строк** OLE DB (провсет) построение объекта ADO **Recordset** (), создание объекта Recordset ADO (Адорс), \*\*\*\* будет иметь следующие три основные операции:</span><span class="sxs-lookup"><span data-stu-id="8f672-121">Given an OLE DB **Rowset** object (pRowset ), the construction of an ADO **Recordset** object (), the construction of an ADO **Recordset** object (adoRs ) amounts to the following three basic operations:</span></span>

1. <span data-ttu-id="8f672-122">Создайте объект ADO **Recordset** :</span><span class="sxs-lookup"><span data-stu-id="8f672-122">Create an ADO **Recordset** object:</span></span>
    
   ```vb
    Recordset20Ptr adoRs;
    adoRs.CreateInstance(__uuidof(Recordset));
   ```
2. <span data-ttu-id="8f672-123">ЗаПросите интерфейс **иадорекордсетконструктион** для объекта **Recordset** :</span><span class="sxs-lookup"><span data-stu-id="8f672-123">Query the **IADORecordsetConstruction** interface on the **Recordset** object:</span></span>

   ```vb    
    adoRecordsetConstructionPtr adoRsConstruct=NULL;
    adoRs->QueryInterface(__uuidof(ADORecordsetConstruction),
         (void**)&adoRsConstruct);
   ```

3. <span data-ttu-id="8f672-124">ВыЗовите метод Иадорекордсетконструктион::p\_UT Rowset, чтобы задать объект набора строк OLE DB для объекта RECORDSET объекта ADO:</span><span class="sxs-lookup"><span data-stu-id="8f672-124">Call the IADORecordsetConstruction::put\_Rowset property method to set the OLE DB Rowset object on the ADO Recordset object:</span></span>

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
<span data-ttu-id="8f672-125">Объект Result теперь представляет объект **RECORDSET** ADO, созданный на основе объекта **набора строк** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="8f672-125">The resultant object now represents the ADO **Recordset** object constructed from the OLE DB **Rowset** object.</span></span>

<span data-ttu-id="8f672-126">Вы также можете создать объект ADO **Recordset** из **главы** OLE DB или объекта **RowPosition** .</span><span class="sxs-lookup"><span data-stu-id="8f672-126">You can also construct an ADO **Recordset** object from an OLE DB **Chapter** or **RowPosition** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f672-127">Требования</span><span class="sxs-lookup"><span data-stu-id="8f672-127">Requirements</span></span>

- <span data-ttu-id="8f672-128">**Версия:** ADO 2,0 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="8f672-128">**Version:** ADO 2.0 and later</span></span>

- <span data-ttu-id="8f672-129">**Библиотека:** Msado15. dll</span><span class="sxs-lookup"><span data-stu-id="8f672-129">**Library:** msado15.dll</span></span>

- <span data-ttu-id="8f672-130">**UUID:** 00000283-0000-0010-8000-00AA006D2EA4</span><span class="sxs-lookup"><span data-stu-id="8f672-130">**UUID:** 00000283-0000-0010-8000-00AA006D2EA4</span></span>

