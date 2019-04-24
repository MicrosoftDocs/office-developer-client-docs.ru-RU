---
title: Свойство DBEngine. DefaultPassword (DAO)
TOCTitle: DefaultPassword Property
ms:assetid: 189e34f3-d573-c75f-8be2-d98c50df8a52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845616(v=office.15)
ms:contentKeyID: 48543478
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 72e73d29129c749d5479e2c7b17827f13adb4847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294360"
---
# <a name="dbenginedefaultpassword-property-dao"></a><span data-ttu-id="23f88-102">Свойство DBEngine. DefaultPassword (DAO)</span><span class="sxs-lookup"><span data-stu-id="23f88-102">DBEngine.DefaultPassword property (DAO)</span></span>


<span data-ttu-id="23f88-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="23f88-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="23f88-104">Задает пароль, используемый для создания **рабочей области** по умолчанию при ее инициализации.</span><span class="sxs-lookup"><span data-stu-id="23f88-104">Sets the password used to create the default **Workspace** when it is initialized.</span></span> <span data-ttu-id="23f88-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="23f88-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="23f88-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23f88-106">Syntax</span></span>

<span data-ttu-id="23f88-107">*Expression* . DefaultPassword</span><span class="sxs-lookup"><span data-stu-id="23f88-107">*expression* .DefaultPassword</span></span>

<span data-ttu-id="23f88-108">*Expression (выражение* ) Переменная, представляющая объект **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="23f88-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="23f88-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="23f88-109">Remarks</span></span>

<span data-ttu-id="23f88-110">Параметр **DefaultPassword** имеет тип данных String, длина которого не может превышать 20 символов.</span><span class="sxs-lookup"><span data-stu-id="23f88-110">The setting for **DefaultPassword** is a String data type that can be up to 20 characters long.</span></span> <span data-ttu-id="23f88-111">Он может содержать любой символ, кроме ASCII 0.</span><span class="sxs-lookup"><span data-stu-id="23f88-111">It can contain any character except ASCII 0.</span></span>


> [!NOTE]
> <span data-ttu-id="23f88-112">Используйте надежные пароли, объединяющие прописные и строчные буквы, цифры и символы.</span><span class="sxs-lookup"><span data-stu-id="23f88-112">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="23f88-113">В слабых паролях эти элементы не комбинируются.</span><span class="sxs-lookup"><span data-stu-id="23f88-113">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="23f88-114">Надежный пароль: Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="23f88-114">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="23f88-115">Слабый пароль: House27.</span><span class="sxs-lookup"><span data-stu-id="23f88-115">Weak password: House27.</span></span> <span data-ttu-id="23f88-116">Используйте надежный пароль, который можно запомнить, чтобы не записывать его.</span><span class="sxs-lookup"><span data-stu-id="23f88-116">Use a strong password that you can remember so that you don't have to write it down.</span></span>

<span data-ttu-id="23f88-117">По умолчанию для свойства **DefaultUser** задано значение "admin", а для свойства **DefaultPassword** задана строка нулевой длины ("").</span><span class="sxs-lookup"><span data-stu-id="23f88-117">By default, the **DefaultUser** property is set to "admin" and the **DefaultPassword** property is set to a zero-length string ("").</span></span>

<span data-ttu-id="23f88-118">Как правило, метод **CreateWorkspace** используется для создания объекта **Workspace** с заданными именем пользователя и паролем.</span><span class="sxs-lookup"><span data-stu-id="23f88-118">Typically, you use the **CreateWorkspace** method to create a **Workspace** object with a given user name and password.</span></span> <span data-ttu-id="23f88-119">Однако для обеспечения обратной совместимости с более ранними версиями и удобства при отсутствии защищенной базы данных ядро СУБД Microsoft Access автоматически создает объект **рабочей области** по умолчанию, если он еще не открыт.</span><span class="sxs-lookup"><span data-stu-id="23f88-119">However, for backward compatibility with earlier versions and for convenience when you don't implement a secured database, the Microsoft Access database engine automatically creates a default **Workspace** object when needed if one isn't already open.</span></span> <span data-ttu-id="23f88-120">В этом случае значения свойств **DefaultUser** и **DefaultPassword** определяют пользователя и пароль для объекта **рабочей области** по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="23f88-120">In this case, the **DefaultUser** and **DefaultPassword** property values define the user and password for the default **Workspace** object.</span></span>

<span data-ttu-id="23f88-121">Чтобы это свойство вступило в силу, необходимо задать его перед вызовом методов DAO.</span><span class="sxs-lookup"><span data-stu-id="23f88-121">For this property to take effect, you should set it before calling any DAO methods.</span></span>

