---
title: Обновление данных (справочник по базам данных Access для настольных ПК)
TOCTitle: Updating Data
ms:assetid: 02e82066-77c8-cbb2-db28-98e2fc94404c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248794(v=office.15)
ms:contentKeyID: 48542970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8e6989468e23fc1c9c611eb091172822a6ffe938
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313569"
---
# <a name="updating-data"></a><span data-ttu-id="0e480-102">Обновление данных</span><span class="sxs-lookup"><span data-stu-id="0e480-102">Updating data</span></span>


<span data-ttu-id="0e480-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e480-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e480-104">Поведение и функциональность обновления в значительной степени зависят от режима обновления (типа блокировки), типа курсора и расположения курсора.</span><span class="sxs-lookup"><span data-stu-id="0e480-104">Update behavior and functionality is largely dependent upon update mode (lock type), cursor type, and cursor location.</span></span>

<span data-ttu-id="0e480-105">Используйте метод **Update,** чтобы сохранить все изменения, внесенные в текущую запись объекта **Recordset** после вызова метода **AddNew** или после изменения значений полей в существующей записи.</span><span class="sxs-lookup"><span data-stu-id="0e480-105">Use the **Update** method to save any changes you have made to the current record of a **Recordset** object since calling the **AddNew** method or since changing any field values in an existing record.</span></span> <span data-ttu-id="0e480-106">Объект **Recordset** должен поддерживать обновления.</span><span class="sxs-lookup"><span data-stu-id="0e480-106">The **Recordset** object must support updates.</span></span>

<span data-ttu-id="0e480-107">Если объект **Recordset** поддерживает пакетное обновление, можно кэшировать несколько изменений в одной или нескольких записях локально, пока не будет вызываться **метод UpdateBatch.**</span><span class="sxs-lookup"><span data-stu-id="0e480-107">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the **UpdateBatch** method.</span></span> <span data-ttu-id="0e480-108">Если вы редактируете текущую запись или добавляете новую запись при вызове метода **UpdateBatch,** ADO будет автоматически вызывать метод **Update,** чтобы сохранить все ожидающие изменения текущей записи перед передачей пакетных изменений поставщику.</span><span class="sxs-lookup"><span data-stu-id="0e480-108">If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

<span data-ttu-id="0e480-109">Текущая запись остается текущей после вызова методов **Update** или **UpdateBatch.**</span><span class="sxs-lookup"><span data-stu-id="0e480-109">The current record remains current after you call the **Update** or **UpdateBatch** methods.</span></span>

<span data-ttu-id="0e480-110">В этой статье содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="0e480-110">This section includes the following topics:</span></span>

- [<span data-ttu-id="0e480-111">Режим немедленного обновления</span><span class="sxs-lookup"><span data-stu-id="0e480-111">Immediate mode</span></span>](immediate-mode.md)
- [<span data-ttu-id="0e480-112">Обработка транзакций</span><span class="sxs-lookup"><span data-stu-id="0e480-112">Transaction processing</span></span>](transaction-processing.md)
- [<span data-ttu-id="0e480-113">Batch mode (ADO)</span><span class="sxs-lookup"><span data-stu-id="0e480-113">Batch mode (ADO)</span></span>](batch-mode.md)

