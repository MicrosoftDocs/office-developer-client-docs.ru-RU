---
title: Обновление данных (Справочник по для настольных баз данных Access)
TOCTitle: Updating Data
ms:assetid: 02e82066-77c8-cbb2-db28-98e2fc94404c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248794(v=office.15)
ms:contentKeyID: 48542970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2f507cb7d8939a4d4da65b570ae8e2db53cc8c7c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480682"
---
# <a name="updating-data"></a><span data-ttu-id="a1923-102">Updating Data</span><span class="sxs-lookup"><span data-stu-id="a1923-102">Updating Data</span></span>


<span data-ttu-id="a1923-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1923-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a1923-104">Функциональность и поведение обновления во многом зависит от обновление режима (тип блокировки), тип курсора и положение курсора.</span><span class="sxs-lookup"><span data-stu-id="a1923-104">Update behavior and functionality is largely dependent upon update mode (lock type), cursor type, and cursor location.</span></span>

<span data-ttu-id="a1923-105">Используйте метод **Update** , чтобы сохранить все изменения, внесенные в текущую запись объекта **набора записей** с момента вызова метода **AddNew** или после изменения значения поля в существующей записи.</span><span class="sxs-lookup"><span data-stu-id="a1923-105">Use the **Update** method to save any changes you have made to the current record of a **Recordset** object since calling the **AddNew** method or since changing any field values in an existing record.</span></span> <span data-ttu-id="a1923-106">Объект **набора записей** должен поддерживать обновлений.</span><span class="sxs-lookup"><span data-stu-id="a1923-106">The **Recordset** object must support updates.</span></span>

<span data-ttu-id="a1923-107">Если объект **набора записей** поддерживает пакетного обновления, можно кэшировать внесение нескольких изменений в одну или несколько записей локально до вызова метода **UpdateBatch** .</span><span class="sxs-lookup"><span data-stu-id="a1923-107">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the **UpdateBatch** method.</span></span> <span data-ttu-id="a1923-108">При изменении текущей записи или добавления новой записи при вызове метода **UpdateBatch** , ADO автоматически будет вызвать метод **Update** для сохранения всех ожидающих изменений в текущей записи перед передачей пакетные изменения Поставщик.</span><span class="sxs-lookup"><span data-stu-id="a1923-108">If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

<span data-ttu-id="a1923-109">Текущая запись остается текущей после вызова метода **Update** или **UpdateBatch** .</span><span class="sxs-lookup"><span data-stu-id="a1923-109">The current record remains current after you call the **Update** or **UpdateBatch** methods.</span></span>

