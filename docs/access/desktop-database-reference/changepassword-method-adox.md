---
title: Изменение пароля метод (ADOX)
TOCTitle: ChangePassword Method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 34de673d29d160c715c8e2617d0e2a75e3843904
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872237"
---
# <a name="changepassword-method-adox"></a><span data-ttu-id="31c47-102">Изменение пароля метод (ADOX)</span><span class="sxs-lookup"><span data-stu-id="31c47-102">ChangePassword Method (ADOX)</span></span>


<span data-ttu-id="31c47-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="31c47-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="31c47-104">Изменение пароля для учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="31c47-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="31c47-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31c47-105">Syntax</span></span>

<span data-ttu-id="31c47-106">*Пользователь*. Изменение пароля*Старый_пароль*, *Новый_пароль*</span><span class="sxs-lookup"><span data-stu-id="31c47-106">*User*.ChangePassword*OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="31c47-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="31c47-107">Parameters</span></span>

  - <span data-ttu-id="31c47-108">*Старый_пароль*</span><span class="sxs-lookup"><span data-stu-id="31c47-108">*OldPassword*</span></span>

  - <span data-ttu-id="31c47-109">**Строковое** значение, задающее существующий пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="31c47-109">A **String** value that specifies the user's existing password.</span></span> <span data-ttu-id="31c47-110">Если у пользователя нет в настоящее время пароль, укажите пустую строку ("») для *Старый_пароль*.</span><span class="sxs-lookup"><span data-stu-id="31c47-110">If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>

  - <span data-ttu-id="31c47-111">*Новый_пароль*</span><span class="sxs-lookup"><span data-stu-id="31c47-111">*NewPassword*</span></span>

  - <span data-ttu-id="31c47-112">**Строковое** значение, задающее новый пароль.</span><span class="sxs-lookup"><span data-stu-id="31c47-112">A **String** value that specifies the new password.</span></span>

## <a name="remarks"></a><span data-ttu-id="31c47-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="31c47-113">Remarks</span></span>

<span data-ttu-id="31c47-114">По соображениям безопасности старый пароль должен быть указан в дополнение к новый пароль.</span><span class="sxs-lookup"><span data-stu-id="31c47-114">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="31c47-115">Если поставщик поддерживает администрирования свойства доверенного лица, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="31c47-115">An error will occur if the provider does not support the administration of trustee properties.</span></span>

