---
title: Указание числа потоков на процессор в IIS
TOCTitle: Specifying threads per processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 57e4b6228588af7f0d58caf53d3e093e824c7854
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308591"
---
# <a name="specifying-threads-per-processor-on-iis"></a><span data-ttu-id="e1fea-102">Указание числа потоков на процессор в IIS</span><span class="sxs-lookup"><span data-stu-id="e1fea-102">Specifying threads per processor on IIS</span></span>


<span data-ttu-id="e1fea-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e1fea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e1fea-104">При использовании RDS с службы IIS 4.0 или более поздним числом потоков, созданных для каждого процессора, можно управлять, манипулируя реестром на веб-сервере.</span><span class="sxs-lookup"><span data-stu-id="e1fea-104">When using RDS with Internet Information Services 4.0 or later, the number of threads created per processor can be controlled by manipulating the registry on the web server.</span></span> <span data-ttu-id="e1fea-105">Количество потоков на процессор может повлиять на производительность в высокой ситуации с трафиком или в ситуациях с низким трафиком с большими размерами запросов.</span><span class="sxs-lookup"><span data-stu-id="e1fea-105">The number of threads per processor can affect performance in a high traffic situation, or in low traffic situations with large query sizes.</span></span> <span data-ttu-id="e1fea-106">Пользователю следует поэкспериментировать для наилучших результатов.</span><span class="sxs-lookup"><span data-stu-id="e1fea-106">The user should experiment for best results.</span></span>

<span data-ttu-id="e1fea-107">Метод, используемый для определения и изменения значения по умолчанию для этого параметра, зависит от конфигурации сервера IIS 4.0.</span><span class="sxs-lookup"><span data-stu-id="e1fea-107">The method used to determine and change the default value for this setting depends upon the configuration of the IIS 4.0 server.</span></span>

<span data-ttu-id="e1fea-108">С помощью MDAC 2.1.2.4202.3 (GA) или более поздней установки на сервере IIS, RDS использует те же службы компонентов (или службы транзакций Майкрософт, если вы используете Windows NT) пул потоков, как и скрипты ASP.</span><span class="sxs-lookup"><span data-stu-id="e1fea-108">With MDAC 2.1.2.4202.3 (GA) or later installed on the IIS server, RDS uses the same Component Services (or Microsoft Transaction Services, if you are using Windows NT) thread pool as ASP scripts use.</span></span> <span data-ttu-id="e1fea-109">Значение по умолчанию для количества потоков в процессоре — 10.</span><span class="sxs-lookup"><span data-stu-id="e1fea-109">The default value for the number of threads per processor is 10.</span></span> <span data-ttu-id="e1fea-110">Чтобы изменить значение по умолчанию, необходимо добавить в реестр серверов следующий ключ:</span><span class="sxs-lookup"><span data-stu-id="e1fea-110">To change the default, you must add the following key to the server registry:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

<span data-ttu-id="e1fea-111">где *MaxPoolThreads* — это \_ DWORD REG.</span><span class="sxs-lookup"><span data-stu-id="e1fea-111">where *MaxPoolThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="e1fea-112">*MaxPoolThreads* не появляется в реестре, если он не добавлен специально.</span><span class="sxs-lookup"><span data-stu-id="e1fea-112">*MaxPoolThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="e1fea-113">Допустимые значения варьируются от 5 до рекомендуемого максимума 20.</span><span class="sxs-lookup"><span data-stu-id="e1fea-113">Valid values range from 5 to a recommended maximum of 20.</span></span> <span data-ttu-id="e1fea-114">Если значение, указанное ключом реестра, превышает значение *ключа PoolThreadLimit* (расположено по тому же пути), то используется *значение PoolThreadLimit.*</span><span class="sxs-lookup"><span data-stu-id="e1fea-114">If the value specified by the registry key is greater than the value of the *PoolThreadLimit* key (located under the same path), then *PoolThreadLimit* value is used.</span></span>

<span data-ttu-id="e1fea-115">Кроме того, если на сервере IIS установленО значение MDAC 2.1 2.1.1.1.3711.11 (GA) или ранее, значение по умолчанию для количества потоков на процессоре составляет 6.</span><span class="sxs-lookup"><span data-stu-id="e1fea-115">Alternatively, if MDAC 2.1 2.1.1.3711.11 (GA) or earlier is installed on the IIS server, the default value for the number of threads per processor is 6.</span></span> <span data-ttu-id="e1fea-116">Чтобы изменить значение по умолчанию, необходимо добавить в реестр на сервере IIS следующий ключ:</span><span class="sxs-lookup"><span data-stu-id="e1fea-116">To change the default, you must add the following key to the registry on the IIS server:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

<span data-ttu-id="e1fea-117">где *ADCThreads* — это \_ DWORD REG.</span><span class="sxs-lookup"><span data-stu-id="e1fea-117">where *ADCThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="e1fea-118">*ADCThreads* не отображаются в реестре, если они не будут специально добавлены.</span><span class="sxs-lookup"><span data-stu-id="e1fea-118">*ADCThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="e1fea-119">Диапазон допустимого значения составляет от 1 до 50.</span><span class="sxs-lookup"><span data-stu-id="e1fea-119">The range of valid values is 1 to 50.</span></span> <span data-ttu-id="e1fea-120">Если значение, указанное ключом реестра, превышает 50, то используется максимальное значение (50).</span><span class="sxs-lookup"><span data-stu-id="e1fea-120">If the value specified by the registry key is greater than 50, then the maximum value is used (50).</span></span>

