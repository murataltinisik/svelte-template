<script>
  import Footer from "../../global/Footer.svelte";
  import Navbar from "../../global/Navbar.svelte";
</script>

<div class="container">
    <!-- NAVBAR -->
    <Navbar />

    <!-- HEAD -->
	<div class="head">
		<h2>Profile</h2>
	</div>

    <!-- CONTENT -->
    <div class="content">
        <!-- ACCOUNT INFORMATION -->
        <div class="relative bg-white shadow account-information my-5">
            <div class="p-3">
                <h1 class="font-bold text-center text-3xl text-gray-900">Pantazi Software</h1>
                <p class="text-center text-sm text-gray-400 font-medium">UI Components Factory</p>

                <div class="flex justify-between items-center my-2 px-6">
                    <a href="" class="text-gray-500 hover:text-gray-900 hover:bg-gray-100 rounded transition duration-150 ease-in font-medium text-sm text-center w-full py-3">Facebook</a>
                    <a href="" class="text-gray-500 hover:text-gray-900 hover:bg-gray-100 rounded transition duration-150 ease-in font-medium text-sm text-center w-full py-3">Twitter</a>
                    <a href="" class="text-gray-500 hover:text-gray-900 hover:bg-gray-100 rounded transition duration-150 ease-in font-medium text-sm text-center w-full py-3">Instagram</a>
                    <a href="" class="text-gray-500 hover:text-gray-900 hover:bg-gray-100 rounded transition duration-150 ease-in font-medium text-sm text-center w-full py-3">Email</a>
                </div>

                <div class="w-full">
                    <h3 class="font-medium text-gray-900 text-left px-6">Recent activites</h3>
                    <div class="mt-5 w-full flex flex-col items-center overflow-hidden text-sm">
                        <a href="#" class="w-full border-t border-gray-100 text-gray-600 py-4 pl-6 pr-3 w-full block hover:bg-gray-100 transition duration-150">
                            <img src="https://avatars0.githubusercontent.com/u/35900628?v=4" alt="" class="rounded-full h-6 shadow-md inline-block mr-2">
                                Updated his status
                                <span class="text-gray-500 text-xs">24 min ago</span>
                        </a>

                        <a href="#" class="w-full border-t border-gray-100 text-gray-600 py-4 pl-6 pr-3 w-full block hover:bg-gray-100 transition duration-150">
                            <img src="https://avatars0.githubusercontent.com/u/35900628?v=4" alt="" class="rounded-full h-6 shadow-md inline-block mr-2">
                                Added new profile picture
                                <span class="text-gray-500 text-xs">42 min ago</span>
                        </a>

                        <a href="#" class="w-full border-t border-gray-100 text-gray-600 py-4 pl-6 pr-3 w-full block hover:bg-gray-100 transition duration-150">
                            <img src="https://avatars0.githubusercontent.com/u/35900628?v=4" alt="" class="rounded-full h-6 shadow-md inline-block mr-2">
                            Posted new article in <span class="font-bold">#Web Dev</span>
                            <span class="text-gray-500 text-xs">49 min ago</span>
                        </a>

                        <a href="#" class="w-full border-t border-gray-100 text-gray-600 py-4 pl-6 pr-3 w-full block hover:bg-gray-100 transition duration-150">
                            <img src="https://avatars0.githubusercontent.com/u/35900628?v=4" alt="" class="rounded-full h-6 shadow-md inline-block mr-2">
                            Edited website settings
                            <span class="text-gray-500 text-xs">1 day ago</span>
                        </a>

                        <a href="#" class="w-full border-t border-gray-100 text-gray-600 py-4 pl-6 pr-3 w-full block hover:bg-gray-100 transition duration-150 overflow-hidden">
                            <img src="https://avatars0.githubusercontent.com/u/35900628?v=4" alt="" class="rounded-full h-6 shadow-md inline-block mr-2">
                            Added new rank
                            <span class="text-gray-500 text-xs">5 days ago</span>
                        </a>
                    </div>
                </div>
            </div>
        </div>

        <!-- PROFILE FORM -->
        <div class="profile-form">
            <div class="bg-white rounded shadow-lg p-4 px-4 md:p-8 mb-6">
                <div class="grid gap-4 gap-y-2 text-sm grid-cols-1 lg:grid-cols-3">
                    <div class="lg:col-span-3">
                        <div class="grid gap-4 gap-y-2 text-sm grid-cols-1 md:grid-cols-5">
                            <div class="md:col-span-5">
                                <label for="full_name">Full Name</label>
                                <input type="text" name="full_name" id="full_name" class="h-10 border mt-1 rounded px-4 w-full bg-gray-50" value="" />
                            </div>
            
                            <div class="md:col-span-5">
                                <label for="email">Email Address</label>
                                <input type="text" name="email" id="email" class="h-10 border mt-1 rounded px-4 w-full bg-gray-50" value="" placeholder="email@domain.com" />
                            </div>
            
                                <div class="md:col-span-2">
                                    <label for="address">Old Password</label>
                                    <input type="text" name="address" id="address" class="h-10 border mt-1 rounded px-4 w-full bg-gray-50" value="" placeholder="" />
                                </div>
                    
                                <div class="md:col-span-2">
                                    <label for="city">New Password</label>
                                    <input type="text" name="city" id="city" class="h-10 border mt-1 rounded px-4 w-full bg-gray-50" value="" placeholder="" />
                                </div>
        
                                <div class="md:col-span-2">
                                    <label for="city">New Password Confirm</label>
                                    <input type="text" name="city" id="city" class="h-10 border mt-1 rounded px-4 w-full bg-gray-50" value="" placeholder="" />
                                </div>
                            
                            <div class="md:col-span-5 text-right">
                                <div class="inline-flex items-end">
                                    <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">Save</button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <button type="button" class="focus:outline-none text-white bg-red-700 hover:bg-red-800 focus:ring-4 focus:ring-red-300 font-medium rounded-lg text-sm px-5 py-2.5 mr-2 mb-2 dark:bg-red-600 dark:hover:bg-red-700 dark:focus:ring-red-900">
                Delete Account
            </button>
        </div>
    </div>

    <!-- FOOTER -->
    <Footer/>
</div>

<style lang="scss">
    @import url('../../app.css');

    .container{
        .content{
            display: flex;
            align-items: flex-start;
            justify-content: space-between;

            .account-information{
                width: 30%;   
            }

            .profile-form{
                width: 65%;
            }
        }
    }
</style>