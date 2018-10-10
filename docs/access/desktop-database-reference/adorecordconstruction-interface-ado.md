---
title: ADORecordConstruction Interface (ADO)
TOCTitle: ADORecordConstruction Interface (ADO)
ms:assetid: 3f0afbdb-f1c4-e44e-7c0f-a0c4cee554a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249175(v=office.15)
ms:contentKeyID: 48544387
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 44272067d8018836fd7eb3d6cfaa762780f69868
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481482"
---
# <a name="adorecordconstruction-interface-ado"></a><span data-ttu-id="fadc0-102">ADORecordConstruction Interface (ADO)</span><span class="sxs-lookup"><span data-stu-id="fadc0-102">ADORecordConstruction Interface (ADO)</span></span>


<span data-ttu-id="fadc0-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fadc0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fadc0-104">Интерфейс **ADORecordConstruction** используется для создания объекта ADO **записи** из объекта OLE DB **строки** в приложении C/C++.</span><span class="sxs-lookup"><span data-stu-id="fadc0-104">The **ADORecordConstruction** interface is used to construct an ADO **Record** object from an OLE DB **Row** object in a C/C++ application.</span></span>

<span data-ttu-id="fadc0-105">Этот интерфейс поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="fadc0-105">This interface supports the following properties:</span></span>

## <a name="properties"></a><span data-ttu-id="fadc0-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="fadc0-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fadc0-107"><a href="parentrow-property-ado.md">ParentRow</a></span><span class="sxs-lookup"><span data-stu-id="fadc0-107"><a href="parentrow-property-ado.md">ParentRow</a></span></span></p></td>
<td><p><span data-ttu-id="fadc0-108">Только для записи.</span><span class="sxs-lookup"><span data-stu-id="fadc0-108">Write-only.</span></span><br />
<span data-ttu-id="fadc0-109">Задает контейнер объекта OLE DB <strong>строку</strong> на этот объект ADO <strong>записи</strong> .</span><span class="sxs-lookup"><span data-stu-id="fadc0-109">Sets the container of an OLE DB <strong>Row</strong> object on this ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fadc0-110"><a href="row-property-ado.md">Строка</a></span><span class="sxs-lookup"><span data-stu-id="fadc0-110"><a href="row-property-ado.md">Row</a></span></span></p></td>
<td><p><span data-ttu-id="fadc0-111">Чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="fadc0-111">Read/Write.</span></span><br />
<span data-ttu-id="fadc0-112">Получает или задает объект OLE DB <strong>строку</strong> из/на этот объект ADO <strong>записи</strong> .</span><span class="sxs-lookup"><span data-stu-id="fadc0-112">Gets/sets an OLE DB <strong>Row</strong> object from/on this ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a><span data-ttu-id="fadc0-113">Методы</span><span class="sxs-lookup"><span data-stu-id="fadc0-113">Methods</span></span>

<span data-ttu-id="fadc0-114">Отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fadc0-114">None.</span></span>

## <a name="events"></a><span data-ttu-id="fadc0-115">События</span><span class="sxs-lookup"><span data-stu-id="fadc0-115">Events</span></span>

<span data-ttu-id="fadc0-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="fadc0-116">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="fadc0-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="fadc0-117">Remarks</span></span>

<span data-ttu-id="fadc0-118">Заданным объекта OLE DB **строки** (pRow), конструкции (объект ADO **записи** ), конструирование объекта ADO **записи** (adoR) объемов для трех основных операций:</span><span class="sxs-lookup"><span data-stu-id="fadc0-118">Given an OLE DB **Row** object (pRow), the construction of an ADO **Record** object (), the construction of an ADO **Record** object (adoR), amounts to the following three basic operations:</span></span>

1.  <span data-ttu-id="fadc0-119">Создайте объект ADO **записи** :</span><span class="sxs-lookup"><span data-stu-id="fadc0-119">Create an ADO **Record** object:</span></span>
    
    ```vb
        _RecordPtr adoR;
        adoRs.CreateInstance(__uuidof(_Record));
    ```

2.  <span data-ttu-id="fadc0-120">Запрос интерфейс **IADORecordConstruction** объекта **записи** :</span><span class="sxs-lookup"><span data-stu-id="fadc0-120">Query the **IADORecordConstruction** interface on the **Record** object:</span></span>
    
    ```vb
        adoRecordConstructionPtr adoRConstruct=NULL;
        adoR->QueryInterface(__uuidof(ADORecordConstruction),
                            (void**)&adoRConstruct);
    ```

3.  <span data-ttu-id="fadc0-121">Вызов **IADORecordConstruction::put\_строки** метод свойства, чтобы установить для объекта OLE DB **строку** на объект ADO **записи** :</span><span class="sxs-lookup"><span data-stu-id="fadc0-121">Call the **IADORecordConstruction::put\_Row** property method to set the OLE DB **Row** object on the ADO **Record** object:</span></span>
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
<span data-ttu-id="fadc0-122">Объект результирующее **adoR** теперь представляет объект ADO **записи** , созданный из объекта OLE DB **строки** .</span><span class="sxs-lookup"><span data-stu-id="fadc0-122">The resultant **adoR** object now represents the ADO **Record** object constructed from the OLE DB **Row** object.</span></span>

<span data-ttu-id="fadc0-123">Объект ADO **записи** также могут быть созданы из контейнера OLE DB **строки** объекта.</span><span class="sxs-lookup"><span data-stu-id="fadc0-123">An ADO **Record** object can also be constructed from the container of an OLE DB **Row** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="fadc0-124">Требования</span><span class="sxs-lookup"><span data-stu-id="fadc0-124">Requirements</span></span>

<span data-ttu-id="fadc0-125">**Версия:** ADO 2.0 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="fadc0-125">**Version:** ADO 2.0 and later</span></span>

<span data-ttu-id="fadc0-126">**Библиотеки:** msado15.dll</span><span class="sxs-lookup"><span data-stu-id="fadc0-126">**Library:** msado15.dll</span></span>

<span data-ttu-id="fadc0-127">**UUID:** 00000567-0000-0010-8000-00AA006D2EA4</span><span class="sxs-lookup"><span data-stu-id="fadc0-127">**UUID:** 00000567-0000-0010-8000-00AA006D2EA4</span></span>

