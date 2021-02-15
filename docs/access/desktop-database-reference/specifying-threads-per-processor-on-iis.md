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
# <a name="specifying-threads-per-processor-on-iis"></a><span data-ttu-id="82476-102">Указание числа потоков на процессор в IIS</span><span class="sxs-lookup"><span data-stu-id="82476-102">Specifying threads per processor on IIS</span></span>


<span data-ttu-id="82476-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="82476-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="82476-104">При использовании RDS со службами Internet Information Services 4.0 или более поздней, количество потоков, созданных для каждого процессора, можно контролировать с помощью реестра на веб-сервере.</span><span class="sxs-lookup"><span data-stu-id="82476-104">When using RDS with Internet Information Services 4.0 or later, the number of threads created per processor can be controlled by manipulating the registry on the web server.</span></span> <span data-ttu-id="82476-105">Число потоков на процессор может влиять на производительность в условиях высокого трафика или при низком трафике с большими размерами запросов.</span><span class="sxs-lookup"><span data-stu-id="82476-105">The number of threads per processor can affect performance in a high traffic situation, or in low traffic situations with large query sizes.</span></span> <span data-ttu-id="82476-106">Для наилучших результатов пользователю следует поэкспериментировать.</span><span class="sxs-lookup"><span data-stu-id="82476-106">The user should experiment for best results.</span></span>

<span data-ttu-id="82476-107">Метод, используемый для определения и изменения значения по умолчанию для этого параметра, зависит от конфигурации сервера IIS 4.0.</span><span class="sxs-lookup"><span data-stu-id="82476-107">The method used to determine and change the default value for this setting depends upon the configuration of the IIS 4.0 server.</span></span>

<span data-ttu-id="82476-108">При установке MDAC 2.1.2.4202.3 или более поздней установки на сервер IIS RDS использует те же службы компонентов (или службы транзакций Майкрософт, если вы используете пул потоков Windows NT), что и сценарии ASP.</span><span class="sxs-lookup"><span data-stu-id="82476-108">With MDAC 2.1.2.4202.3 (GA) or later installed on the IIS server, RDS uses the same Component Services (or Microsoft Transaction Services, if you are using Windows NT) thread pool as ASP scripts use.</span></span> <span data-ttu-id="82476-109">Значение по умолчанию для числа потоков на процессор — 10.</span><span class="sxs-lookup"><span data-stu-id="82476-109">The default value for the number of threads per processor is 10.</span></span> <span data-ttu-id="82476-110">Чтобы изменить значение по умолчанию, необходимо добавить следующий ключ в реестр серверов:</span><span class="sxs-lookup"><span data-stu-id="82476-110">To change the default, you must add the following key to the server registry:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

<span data-ttu-id="82476-111">где *MaxPoolThreads* — это REG \_ DWORD.</span><span class="sxs-lookup"><span data-stu-id="82476-111">where *MaxPoolThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="82476-112">*MaxPoolThreads* не появляется в реестре, если он специально не добавлен.</span><span class="sxs-lookup"><span data-stu-id="82476-112">*MaxPoolThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="82476-113">Допустимые значения: от 5 до рекомендуемого максимума 20.</span><span class="sxs-lookup"><span data-stu-id="82476-113">Valid values range from 5 to a recommended maximum of 20.</span></span> <span data-ttu-id="82476-114">Если значение, указанное в ключе реестра, больше значения ключа *PoolThreadLimit* (расположено по тому же пути), используется значение *PoolThreadLimit.*</span><span class="sxs-lookup"><span data-stu-id="82476-114">If the value specified by the registry key is greater than the value of the *PoolThreadLimit* key (located under the same path), then *PoolThreadLimit* value is used.</span></span>

<span data-ttu-id="82476-115">Кроме того, если MDAC 2.1 2.1.1.3711.11 или более ранней установки установлен на сервер IIS, значение по умолчанию для числа потоков на процессор составляет 6.</span><span class="sxs-lookup"><span data-stu-id="82476-115">Alternatively, if MDAC 2.1 2.1.1.3711.11 (GA) or earlier is installed on the IIS server, the default value for the number of threads per processor is 6.</span></span> <span data-ttu-id="82476-116">Чтобы изменить значение по умолчанию, необходимо добавить следующий ключ в реестр на сервере IIS:</span><span class="sxs-lookup"><span data-stu-id="82476-116">To change the default, you must add the following key to the registry on the IIS server:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

<span data-ttu-id="82476-117">где *ADCThreads* — это REG \_ DWORD.</span><span class="sxs-lookup"><span data-stu-id="82476-117">where *ADCThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="82476-118">*ADCThreads* не появляется в реестре, если он специально не добавлен.</span><span class="sxs-lookup"><span data-stu-id="82476-118">*ADCThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="82476-119">Диапазон допустимого значения — от 1 до 50.</span><span class="sxs-lookup"><span data-stu-id="82476-119">The range of valid values is 1 to 50.</span></span> <span data-ttu-id="82476-120">Если значение, указанное в ключе реестра, превышает 50, используется максимальное значение (50).</span><span class="sxs-lookup"><span data-stu-id="82476-120">If the value specified by the registry key is greater than 50, then the maximum value is used (50).</span></span>

