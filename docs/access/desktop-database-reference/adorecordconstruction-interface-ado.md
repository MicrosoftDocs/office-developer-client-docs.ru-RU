---
title: Интерфейс ADORecordConstruction (ADO)
TOCTitle: ADORecordConstruction interface (ADO)
ms:assetid: 3f0afbdb-f1c4-e44e-7c0f-a0c4cee554a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249175(v=office.15)
ms:contentKeyID: 48544387
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1a53eb107bab0d31606dc161b9f9c910894c5bc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281628"
---
# <a name="adorecordconstruction-interface-ado"></a><span data-ttu-id="6f24c-102">Интерфейс ADORecordConstruction (ADO)</span><span class="sxs-lookup"><span data-stu-id="6f24c-102">ADORecordConstruction interface (ADO)</span></span>


<span data-ttu-id="6f24c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f24c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6f24c-104">Интерфейс **ADORecordConstruction** используется для создания объекта **записи** ADO из объекта **строки** OLE DB в приложении C/C++.</span><span class="sxs-lookup"><span data-stu-id="6f24c-104">The **ADORecordConstruction** interface is used to construct an ADO **Record** object from an OLE DB **Row** object in a C/C++ application.</span></span>

<span data-ttu-id="6f24c-105">Этот интерфейс поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="6f24c-105">This interface supports the following properties:</span></span>

## <a name="properties"></a><span data-ttu-id="6f24c-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="6f24c-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f24c-107"><a href="parentrow-property-ado.md">ParentRow</a></span><span class="sxs-lookup"><span data-stu-id="6f24c-107"><a href="parentrow-property-ado.md">ParentRow</a></span></span></p></td>
<td><p><span data-ttu-id="6f24c-108">Только для записи.</span><span class="sxs-lookup"><span data-stu-id="6f24c-108">Write-only.</span></span><br />
<span data-ttu-id="6f24c-109">Задает контейнер объекта <strong>строки</strong> OLE DB для этого объекта <strong>записи</strong> ADO.</span><span class="sxs-lookup"><span data-stu-id="6f24c-109">Sets the container of an OLE DB <strong>Row</strong> object on this ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f24c-110"><a href="row-property-ado.md">Row</a></span><span class="sxs-lookup"><span data-stu-id="6f24c-110"><a href="row-property-ado.md">Row</a></span></span></p></td>
<td><p><span data-ttu-id="6f24c-111">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="6f24c-111">Read/Write.</span></span><br />
<span data-ttu-id="6f24c-112">Получает или задает объект <strong>строки</strong> OLE DB от или on этого объекта <strong>записи</strong> ADO.</span><span class="sxs-lookup"><span data-stu-id="6f24c-112">Gets/sets an OLE DB <strong>Row</strong> object from/on this ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a><span data-ttu-id="6f24c-113">Методы</span><span class="sxs-lookup"><span data-stu-id="6f24c-113">Methods</span></span>

<span data-ttu-id="6f24c-114">Нет.</span><span class="sxs-lookup"><span data-stu-id="6f24c-114">None.</span></span>

## <a name="events"></a><span data-ttu-id="6f24c-115">События</span><span class="sxs-lookup"><span data-stu-id="6f24c-115">Events</span></span>

<span data-ttu-id="6f24c-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="6f24c-116">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f24c-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="6f24c-117">Remarks</span></span>

<span data-ttu-id="6f24c-118">ПоЛучив объект **строки** OLE DB (пров), создание объекта **записи** ADO (), создание объекта **записи** ADO (Адор), суммы для следующих трех базовых операций:</span><span class="sxs-lookup"><span data-stu-id="6f24c-118">Given an OLE DB **Row** object (pRow), the construction of an ADO **Record** object (), the construction of an ADO **Record** object (adoR), amounts to the following three basic operations:</span></span>

1.  <span data-ttu-id="6f24c-119">Создание объекта **записи** ADO:</span><span class="sxs-lookup"><span data-stu-id="6f24c-119">Create an ADO **Record** object:</span></span>
    
    ```vb
        _RecordPtr adoR;
        adoRs.CreateInstance(__uuidof(_Record));
    ```

2.  <span data-ttu-id="6f24c-120">ЗаПросите интерфейс **иадорекордконструктион** для объекта **Record** :</span><span class="sxs-lookup"><span data-stu-id="6f24c-120">Query the **IADORecordConstruction** interface on the **Record** object:</span></span>
    
    ```vb
        adoRecordConstructionPtr adoRConstruct=NULL;
        adoR->QueryInterface(__uuidof(ADORecordConstruction),
                            (void**)&adoRConstruct);
    ```

3.  <span data-ttu-id="6f24c-121">ВыЗовите метод **иадорекордконструктион::p\_UT Row** , чтобы задать объект **строки** OLE DB для объекта **записи** ADO:</span><span class="sxs-lookup"><span data-stu-id="6f24c-121">Call the **IADORecordConstruction::put\_Row** property method to set the OLE DB **Row** object on the ADO **Record** object:</span></span>
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
<span data-ttu-id="6f24c-122">Объект resultd **Адор** теперь представляет объект **записи** ADO, созданный на основе объекта **строки** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="6f24c-122">The resultant **adoR** object now represents the ADO **Record** object constructed from the OLE DB **Row** object.</span></span>

<span data-ttu-id="6f24c-123">Объект **записи** ADO также может быть создан из контейнера объекта **строки** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="6f24c-123">An ADO **Record** object can also be constructed from the container of an OLE DB **Row** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f24c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="6f24c-124">Requirements</span></span>

<span data-ttu-id="6f24c-125">**Версия:** ADO 2,0 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="6f24c-125">**Version:** ADO 2.0 and later</span></span>

<span data-ttu-id="6f24c-126">**Библиотека:** Msado15. dll</span><span class="sxs-lookup"><span data-stu-id="6f24c-126">**Library:** msado15.dll</span></span>

<span data-ttu-id="6f24c-127">**UUID:** 00000567-0000-0010-8000-00AA006D2EA4</span><span class="sxs-lookup"><span data-stu-id="6f24c-127">**UUID:** 00000567-0000-0010-8000-00AA006D2EA4</span></span>

