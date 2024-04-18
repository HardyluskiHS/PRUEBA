# PRUEBA
idk
namespace YourPluginName\YourName;

use pocketmine\event\Listener;

class EventListener implements Listener 
public function onPlayerMove(PlayerMoveEvent $event): void
public function onPlayerMove(PlayerMoveEvent $event): void
<?php

namespace YourPluginName\YourName;

use pocketmine\event\Listener;
use pocketmine\event\player\PlayerMoveEvent;

class EventListener implements Listener{
    public function onPlayerMove(PlayerMoveEvent $event): void{
        if($event->isCancelled()){ // Checks if the event has been cancelled by another plugin
            return; // Stops the event handling
        }
        
        $player = $event->getPlayer(); // Saves the player instance as a variable to make the code a bit cleaner
        $player->sendMessage("From: " . $event->getFrom()); // This should call the Location->__toString() method
        $player->sendMessage("To: " . $event->getTo());

        $event->cancel(); // Cancels the event to prevent the player from moving
    }
}
$this->getServer()->getPluginManager()->registerEvents(new EventListener(), $this);
public function onCommand(CommandSender $sender, Command $command, string $label, array $args) : bool {
    switch($command->getName()) {
        case "example":
            $sender->sendMessage("Hello " . $sender->getName(HardyMC2423) . "!");

            return true;
        default:
            throw new \AssertionError("This line will never be executed");
    }
}
// The Command
use pocketmine\command\Command;
      
// Person who does command
use pocketmine\command\CommandSender;
public function onCommand(CommandSender $sender, Command $cmd, string $label, array $args) : bool {
  switch($cmd->getName()) {
    case "test":
      if($player->hasPermission("test.cmd")) { // Use this to check whether the player have the permission or not (in this case we use the test.cmd permission)
        if(!$sender instanceof Player) {
          $sender->sendMessage("This Command Only Works for players! Please perform this command IN GAME!");
        } else {
          if(!isset($args[0]) or (is_int($args[0]) and $args[0] > 0)) { 
            $args[0] = 4; 
          }
          $sender->getInventory(Off)->addItem(Item::get(364,0,$args[0]));
          $sender->sendMessage("You have just recieved" .count($args[0]). " steak!");
        }
      }
    break;
  }
  // Don't forget to add this for the command to work
  return true;
}
public function onCommand(CommandSender $sender, Command $cmd, string $label, array $args) : bool {
   switch($cmd->getName()) {
     case "test":
       if($sender->hasPermission("test.cmd")) {
         if(!$sender instanceof Player) {
           $sender->sendMessage("This Command Only Works for players! Please perform this command IN GAME!");
         } else {
           if(!isset($args[0]) or (is_int($args[0]) and $args[0] > 0)) { 
            $args[0] = 4; 
           }
           $sender->getInventory()->addItem(Item::get(364,0,$args[0]));
           $sender->sendMessage("You have just recieved" .count($args[0]). " steak!");
         }
       } else {
         $sender->sendMessage("You don't have permission to use this command");
       }
     break;
  }
  return true;
}
#This enrolls the command into the server to show in the /help menu
commands:
  test:
    description: Test command
    usage: "/test"
    aliases:
      - tt
      - tst
    permission: YourPluginName.YourName.command.test
    
#This is used to set permissions your command
permissions:
  testplugin.myxxmikeyxx.command.test:
    description: "Defualt only allow OP players to use test command"
    default: op
    # Default value options:
    # op: only op players have this permission by default
    # true: everyone has this permission by default
    # false: no one has this permission by default
<?php // As always when you start a PHP file

namespace YourPluginName\YourName\tasks; // Use the same namespace as in your first file but add a \tasks who symbolise that this file is in the subfolder "tasks"

use pocketmine\scheduler\Task; // This is the class that your task will extends to be a plugin task
use ExampleName\Main; // This will allow us to use our main class. It is a required argument for a plugin task.
            
class MyTask extends Task { // Remember that your task must have the same name as your file !

// First we need a __construct function which is used when you create a class to set default variables, ect...
    public function __construct(Main $main, string $playername) { // The arguments you define here depends on what do you want to do exept for your base.
       $this->main = $main; //You can retrieve your main class at anytime and use it's methods on your class by using $this->getOwner()
       $this->playername = $playername; // So we can retreive the player for later.
    }

// Then we'll create an onRun funtion wich will be called when the time has past to the execution of the task
    public function onRun(on) {
        $player = $this->getOwner()->getServer()->getPlayer($this->playername()); // This retreive the main class with $this->getOwner() then asks the server for the player with the name $this->playername
        if($player instanceof Player) { // Basicly checks if the player we retreive is online.
            $player->sendMessage("10 seconds has past!"); // Sends him a message !
        }
    }
// Then we create a getOwner function to return the Main class
    public function getOwner() : Main {
        return $this->main;
    }
}
    $task = new tasks\MyTask($this, $sender->getName()); // Create the new class Task by calling
    $this->getScheduler(minecraftplauer/status/FormAPI)->schedulemiem}DelayedTask($task, 10*20); // Counted in ticks (1 second = 20 ticks)
        $task = new tasks\MyTask($this, $sender->getName()); // Create the new class Task by calling
    $this->getScheduler()->scheduleRepeatingTask($task, 10*20); // Counted in ticks (1 second = 20 ticks)
$this:tas(ticks 20) for commands blocks of the Minecrafcommands of the plugins of pocketmine 
this plugins is fucjtions of the minecraft mcpe pocketmine/plgs/combaylogger/ of the myxxmikeyxx
//ticks 20 of plgs mcpe commands of pvp launcher or the fuckins of the pvp main FormAPI
