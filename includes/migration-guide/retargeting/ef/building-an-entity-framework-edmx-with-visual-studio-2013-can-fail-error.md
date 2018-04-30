### <a name="building-an-entity-framework-edmx-with-visual-studio-2013-can-fail-with-error-msb4062-if-using-the-entitydeploysplit-or-entityclean-tasks"></a><span data-ttu-id="911a0-101">如果使用 EntityDeploySplit 或 EntityClean 任务，使用 Visual Studio 2013 生成 Entity Framework edmx 会失败，错误编码为 MSB4062</span><span class="sxs-lookup"><span data-stu-id="911a0-101">Building an Entity Framework edmx with Visual Studio 2013 can fail with error MSB4062 if using the EntityDeploySplit or EntityClean tasks</span></span>

|   |   |
|---|---|
|<span data-ttu-id="911a0-102">详细信息</span><span class="sxs-lookup"><span data-stu-id="911a0-102">Details</span></span>|<span data-ttu-id="911a0-103">MSBuild 12.0 工具（包括在 Visual Studio 2013 中）更改了 MSBuild 文件位置，使得旧 Entity Framework 目标文件变为无效文件。</span><span class="sxs-lookup"><span data-stu-id="911a0-103">MSBuild 12.0 tools (included in Visual Studio 2013) changed MSBuild file locations, causing older Entity Framework targets files to be invalid.</span></span> <span data-ttu-id="911a0-104">结果是 <code>EntityDeploySplit</code> 和 <code>EntityClean</code> 任务失败，因为它们无法找到 <code>Microsoft.Data.Entity.Build.Tasks.dll</code>。</span><span class="sxs-lookup"><span data-stu-id="911a0-104">The result is that <code>EntityDeploySplit</code> and <code>EntityClean</code> tasks fail because they are unable to find <code>Microsoft.Data.Entity.Build.Tasks.dll</code>.</span></span> <span data-ttu-id="911a0-105">请注意，此中断是由于工具集 (MSBuild/VS) 更改而引起的，并不是因为 .NET Framework 更改。</span><span class="sxs-lookup"><span data-stu-id="911a0-105">Note that this break is because of a toolset (MSBuild/VS) change, not because of a .NET Framework change.</span></span> <span data-ttu-id="911a0-106">它仅在升级开发人员工具时才会发生，仅升级 .NET Framework 不会发生。</span><span class="sxs-lookup"><span data-stu-id="911a0-106">It will only occur when upgrading developer tools, not when merely upgrading the .NET Framework.</span></span>|
|<span data-ttu-id="911a0-107">建议</span><span class="sxs-lookup"><span data-stu-id="911a0-107">Suggestion</span></span>|<span data-ttu-id="911a0-108">从 .NET Framework 4.6 开始，Entity Framework 目标文件已修复，可与新 MSBuild 布局一起使用。</span><span class="sxs-lookup"><span data-stu-id="911a0-108">Entity Framework targets files are fixed to work with the new MSBuild layout beginning in the .NET Framework 4.6.</span></span> <span data-ttu-id="911a0-109">升级到该版本的 Framework 将解决此问题。</span><span class="sxs-lookup"><span data-stu-id="911a0-109">Upgrading to that version of the Framework will fix this issue.</span></span> <span data-ttu-id="911a0-110">或者，可使用[此](http://stackoverflow.com/a/24249247/131944)解决方法直接修补目标文件。</span><span class="sxs-lookup"><span data-stu-id="911a0-110">Alternatively, [this](http://stackoverflow.com/a/24249247/131944) workaround can be used to patch the targets files directly.</span></span>|
|<span data-ttu-id="911a0-111">范围</span><span class="sxs-lookup"><span data-stu-id="911a0-111">Scope</span></span>|<span data-ttu-id="911a0-112">主要</span><span class="sxs-lookup"><span data-stu-id="911a0-112">Major</span></span>|
|<span data-ttu-id="911a0-113">版本</span><span class="sxs-lookup"><span data-stu-id="911a0-113">Version</span></span>|<span data-ttu-id="911a0-114">4.5.1</span><span class="sxs-lookup"><span data-stu-id="911a0-114">4.5.1</span></span>|
|<span data-ttu-id="911a0-115">类型</span><span class="sxs-lookup"><span data-stu-id="911a0-115">Type</span></span>|<span data-ttu-id="911a0-116">重定目标</span><span class="sxs-lookup"><span data-stu-id="911a0-116">Retargeting</span></span>|
