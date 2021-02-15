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
# <a name="adorecordconstruction-interface-ado"></a><span data-ttu-id="f6ee9-102">Интерфейс ADORecordConstruction (ADO)</span><span class="sxs-lookup"><span data-stu-id="f6ee9-102">ADORecordConstruction interface (ADO)</span></span>


<span data-ttu-id="f6ee9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f6ee9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f6ee9-104">Интерфейс **ADORecordConstruction** используется для создания объекта записи **ADO** из объекта строки OLE **DB** в приложении C/C++.</span><span class="sxs-lookup"><span data-stu-id="f6ee9-104">The **ADORecordConstruction** interface is used to construct an ADO **Record** object from an OLE DB **Row** object in a C/C++ application.</span></span>

<span data-ttu-id="f6ee9-105">Этот интерфейс поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="f6ee9-105">This interface supports the following properties:</span></span>

## <a name="properties"></a><span data-ttu-id="f6ee9-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="f6ee9-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6ee9-107"><a href="parentrow-property-ado.md">ParentRow</a></span><span class="sxs-lookup"><span data-stu-id="f6ee9-107"><a href="parentrow-property-ado.md">ParentRow</a></span></span></p></td>
<td><p><span data-ttu-id="f6ee9-108">Только для записи.</span><span class="sxs-lookup"><span data-stu-id="f6ee9-108">Write-only.</span></span><br />
<span data-ttu-id="f6ee9-109">Задает контейнер объекта строки OLE <strong>DB</strong> для этого объекта <strong>записи</strong> ADO.</span><span class="sxs-lookup"><span data-stu-id="f6ee9-109">Sets the container of an OLE DB <strong>Row</strong> object on this ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6ee9-110"><a href="row-property-ado.md">Row</a></span><span class="sxs-lookup"><span data-stu-id="f6ee9-110"><a href="row-property-ado.md">Row</a></span></span></p></td>
<td><p><span data-ttu-id="f6ee9-111">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f6ee9-111">Read/Write.</span></span><br />
<span data-ttu-id="f6ee9-112">Получает или задает объект строки OLE <strong>DB</strong> из/на этом объекте <strong>записи</strong> ADO.</span><span class="sxs-lookup"><span data-stu-id="f6ee9-112">Gets/sets an OLE DB <strong>Row</strong> object from/on this ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a><span data-ttu-id="f6ee9-113">Methods</span><span class="sxs-lookup"><span data-stu-id="f6ee9-113">Methods</span></span>

<span data-ttu-id="f6ee9-114">Нет.</span><span class="sxs-lookup"><span data-stu-id="f6ee9-114">None.</span></span>

## <a name="events"></a><span data-ttu-id="f6ee9-115">События</span><span class="sxs-lookup"><span data-stu-id="f6ee9-115">Events</span></span>

<span data-ttu-id="f6ee9-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="f6ee9-116">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6ee9-117">Заметки</span><span class="sxs-lookup"><span data-stu-id="f6ee9-117">Remarks</span></span>

<span data-ttu-id="f6ee9-118">С учетом объекта строки OLE **DB** (pRow) при конструкции объекта записи **ADO** (adoR) конструкция объекта записи ADO (adoR) составляет следующие три основные операции: </span><span class="sxs-lookup"><span data-stu-id="f6ee9-118">Given an OLE DB **Row** object (pRow), the construction of an ADO **Record** object (), the construction of an ADO **Record** object (adoR), amounts to the following three basic operations:</span></span>

1.  <span data-ttu-id="f6ee9-119">Создание объекта **записи** ADO:</span><span class="sxs-lookup"><span data-stu-id="f6ee9-119">Create an ADO **Record** object:</span></span>
    
    ```vb
        _RecordPtr adoR;
        adoRs.CreateInstance(__uuidof(_Record));
    ```

2.  <span data-ttu-id="f6ee9-120">Запрос **интерфейса IADORecordConstruction** объекта **Record:**</span><span class="sxs-lookup"><span data-stu-id="f6ee9-120">Query the **IADORecordConstruction** interface on the **Record** object:</span></span>
    
    ```vb
        adoRecordConstructionPtr adoRConstruct=NULL;
        adoR->QueryInterface(__uuidof(ADORecordConstruction),
                            (void**)&adoRConstruct);
    ```

3.  <span data-ttu-id="f6ee9-121">Вызовите метод свойства **IADORecordConstruction::p ut \_ Row,** чтобы установить объект строки OLE **DB** в объекте ADO **Record:**</span><span class="sxs-lookup"><span data-stu-id="f6ee9-121">Call the **IADORecordConstruction::put\_Row** property method to set the OLE DB **Row** object on the ADO **Record** object:</span></span>
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
<span data-ttu-id="f6ee9-122">После этого **объект adoR** представляет объект записи **ADO,** построенный из объекта строки OLE **DB.**</span><span class="sxs-lookup"><span data-stu-id="f6ee9-122">The resultant **adoR** object now represents the ADO **Record** object constructed from the OLE DB **Row** object.</span></span>

<span data-ttu-id="f6ee9-123">Объект **записи** ADO также можно построить из контейнера объекта строки OLE **DB.**</span><span class="sxs-lookup"><span data-stu-id="f6ee9-123">An ADO **Record** object can also be constructed from the container of an OLE DB **Row** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6ee9-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f6ee9-124">Requirements</span></span>

<span data-ttu-id="f6ee9-125">**Версия:** ADO 2.0 и более поздние</span><span class="sxs-lookup"><span data-stu-id="f6ee9-125">**Version:** ADO 2.0 and later</span></span>

<span data-ttu-id="f6ee9-126">**Библиотека:** msado15.dll</span><span class="sxs-lookup"><span data-stu-id="f6ee9-126">**Library:** msado15.dll</span></span>

<span data-ttu-id="f6ee9-127">**UUID:** 00000567-0000-0010-8000-00AA006D2EA4</span><span class="sxs-lookup"><span data-stu-id="f6ee9-127">**UUID:** 00000567-0000-0010-8000-00AA006D2EA4</span></span>

